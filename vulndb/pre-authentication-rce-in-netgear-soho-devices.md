---
title: Pre-Authentication Remote Code Execution in Netgear SOHO devices
---
Multiple Netgear devices contain a stack buffer overflow in the httpd web server's handling of upgrade_check.cgi, 
which may allow for unauthenticated remote code execution with root privileges.

Many Netgear devices contain an embedded web server, which is provided by the httpd process, 
to provide administrative capabilities. On multiple Netgear devices, this code fails to properly validate
the header size provided to the upgrade_check.cgi handler. Despite copying the header to a fixed-size buffer 
on the stack, the vulnerable code copies an attacker-provided count of bytes from attacker-provided data. 
This allows for remote code execution by way of stack buffer overflow.

By convincing a user to visit a malicious or compromised website, a remote, unauthenticated attacker maybe able 
to execute arbitrary code on a vulnerable device with root privileges.

It has been reported that there is a virus called Glupteba on Windows PCs that exploits the vulnerability.

#### Recommendations

NETGEAR strongly recommends that you download the latest firmware as soon as a firmware update or firmware hotfix is available for your product.

#### References

- [Pre-Authentication Remote Code Execution in Netgear SOHO devices](https://github.com/grimm-co/NotQuite0DayFriday/tree/2776cfb25e2a94ebc39e6518bc9139101f20266d/2020.06.15-netgear)
- [Netgear httpd upgrade_check.cgi stack buffer overflow](https://www.kb.cert.org/vuls/id/576779)
- [Security Advisory for Multiple Vulnerabilities on Some Routers, Mobile Routers, Modems, Gateways, and Extenders](https://kb.netgear.com/000061982/Security-Advisory-for-Multiple-Vulnerabilities-on-Some-Routers-Mobile-Routers-Modems-Gateways-and-Extenders)
