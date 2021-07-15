---
title: An unauthenticated PHP code injection in Seagate NAS products
---
Seagate Business NAS products come with a web-enabled management application. This application lets administrators perform the usual device configuration functions, such as adding users, setting up access control, managing files, and more.
The application is build on the out of date technologies, which are known to have security issues. On top of these technologies sits a custom PHP application, which itself contains a number of security-related issues.

#### Recommendations

It is recommended that consumers of these Seagate Business NAS products (and other products using vulnerable firmware) ensure that devices are not accessible via the public Internet. For internal use, it is recommended that the devices be located behind a firewall configured to allow only a trusted set of IP addresses to connect to the web interface.

During April 2015 Seagate released firmware that attempts to resolve these issues.

#### References

* [Advisory: Seagate NAS Remote Code Execution Vulnerability](https://beyondbinary.io/articles/seagate-nas-rce/)
* [Seagate Business NAS 2014.00319 - Unauthenticated Remote Code Execution](https://www.exploit-db.com/exploits/36202/)

#### Technical details

The custom web application does not appear to maintain session-related information on the web server side. All of the information relevant to a user session is stored inside the session cookie prior to it being encrypted and sent to the browser. The PHP hash inside the cookie contains a number of key/value entries, including the following:

- **username**: this is a string value that represents the name of the user in the current session.
- **is_admin**: this is a string value that can be set to yes or no, and indicates whether the current user is an administrator on the NAS.
- **language**: this is a string value that represents the current user’s chosen language (eg. en_US).

Once a session has been established and the username field is present in the cookie, the system does no further validation of user credentials. This means that if a user can manipulate this value directly, instead of attempting to log in the standard way, they can bypass the login mechanism completely.

Direct modification (or addition) of the is_admin value allows a user to self-elevate to administrative privileges in the web application itself.

The fact that a static session encryption key is in use across all instances of the NAS means that once a user has a valid session cookie on one instance, they can apply that same cookie directly to another instance and acquire the same level of access. In short, once a user is logged in as admin on one instance, they’re effectively admin on every instance.

The language parameter is used to generate a file path that is referenced in the web application PHP code via a call to include(). Manipulation of this parameter allows for exploitation of a local file inclusion vulnerability.

Finally, the web application is being served by an instance of Lighttpd that is running under the context of the root user. Hence, any successful exploitation results in activities being conducted as root.
