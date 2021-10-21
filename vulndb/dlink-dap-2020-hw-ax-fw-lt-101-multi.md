---
title: Multiple vulnerabilities in DAP-2020 H/W rev. Ax with F/W v1.01 and below
---
Following vulnerabilities was discovered in DAP-2020 H/W rev. Ax with F/W v1.01 and below: 
- CVE-2021-27248 - webproc getpage Stack-based Buffer Overflow RCE Vulnerability
- CVE-2021-27249 - WEB_CmdFileList Command Injection Remote Code Execution Vulnerability
- CVE-2021-27250 - Errorpage External Control of File Name Information Disclosure Vulnerability
- CVE-2021-34860 - webproc getpage Directory Traversal Information Disclosure Vulnerability
- CVE-2021-34861 - webproc Stack-based Buffer Overflow Remote Code Execution Vulnerability
- CVE-2021-34862 - webproc var:menu Stack-based Buffer Overflow Remote Code Execution Vulnerability
- CVE-2021-34863 - webproc var:page Stack-based Buffer Overflow Remote Code Execution Vulnerability
- Webupg sessionid Handling Remote Heap-based Buffer Overflow
- Insecure sessionid Generation Remote Session Hijacking Weakness
- Webproc WEB_GetCgiVars() Function Multiple Parameters Remote Stack Buffer Overflows
- Webproc WEB_DisplayPage() Function Multiple Parameter Remote Stack Buffer Overflow
- Webproc main() Function HTTP POST Parameter Handling Remote Stack Buffer Overflow
- WEB_PostObjAuth() Function HTTP POST Parameter Handling Remote Heap Buffer Overflow
- libssap.so COMM_MakeCustomMsg() Function Stack Buffer Overflow

The vulnerabilities allow a remote attacker to take control over device. No authentication required.

#### Recommendations

A firmware update is released by D-Link addresses the vulnerabilities in affected devices. It is strongly recommended all users to install the relevant update.

#### References

* [DAP-2020 : H/W Rev. Ax : F/W v1.01 :: Multiple Vulnerability](https://supportannouncement.us.dlink.com/announcement/publication.aspx?name=SAP10201)
* [D-LinkGATE Remote Code Execution](https://suid.ch/research/DAP-2020_Preauth_RCE_Chain.html)

> CVE-2021-27248,CVE-2021-27249,CVE-2021-27250,CVE-2021-34860,CVE-2021-34861,CVE-2021-34862,CVE-2021-34863
