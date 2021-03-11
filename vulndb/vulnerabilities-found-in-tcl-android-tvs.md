A vulnerability in the TCL Android Smart TV series V8-R851T02-LF1 V295 and below and V8-T658T01-LF1 V373 and below by TCL Technology Group Corporation allows an 
attacker on the adjacent network to arbitrarily browse and download sensitive files over an insecure web server running on port 7989 that lists all files & directories.
An unprivileged remote attacker on the adjacent network, can download most system files, leading to serious critical information disclosure. Also, some TV models and/or 
FW versions may expose the webserver with the entire filesystem accessible on another port. For example, nmap scan for all ports run directly from the TV model U43P6046 
(Android 8.0) showed port 7983 not mentioned in the original CVE description, but containing the same directory listing of the entire filesystem. This webserver is bound 
(at least) to localhost interface and accessible freely to all unprivileged installed apps on the Android such as a regular web browser. Any app can therefore read any files 
of any other apps including Android system settings including sensitive data such as saved passwords, private keys etc.

#### Recommendations

Vendor allegedly patched & performed silent update.

#### References

- [https://support.tcl.com/vulnerabilities-found-in-tcl-android-tvs](https://support.tcl.com/vulnerabilities-found-in-tcl-android-tvs)
- [https://github.com/sickcodes/security/blob/master/advisories/SICK-2020-009.md](https://github.com/sickcodes/security/blob/master/advisories/SICK-2020-009.md)

> CVE-2020-27403
