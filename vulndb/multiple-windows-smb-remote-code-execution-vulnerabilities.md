---
title: SMB server allows remote attackers to execute arbitrary code via crafted packets
---
Remote code execution vulnerabilities exist in the way that the Microsoft Server Message Block 1.0 (SMBv1) server handles certain requests. An attacker who successfully exploited the vulnerabilities could gain the ability to execute code on the target server.
To exploit the vulnerability, in most situations, an unauthenticated attacker could send a specially crafted packet to a targeted SMBv1 server.

Alongside the EternalBlue exploit the DoublePulsar implant tool is used. DoublePulsar is a backdoor implant tool developed by the U.S. National Security Agency (NSA) Equation Group that was leaked by The Shadow Brokers in early 2017. The implant runs in kernel mode, which grants cybercriminals a high level of control over the computer system.

#### Recommendations

- Make sure your system is patched against the EternalBlue exploit, otherwise disable SMBv1.
- If your system is infected with DoublePulsar already, run a removal tool ASAP 

#### References

* [ESET Stops WannaCryptor, WannaCry and EternalBlue](https://support.eset.com/kb6481/)
* [How to enable and disable SMBv1, SMBv2, and SMBv3 in Windows and Windows Server](https://support.microsoft.com/en-us/help/2696547/how-to-enable-and-disable-smbv1-smbv2-and-smbv3-in-windows-and-windows)
* [Microsoft Security Bulletin MS17-010](https://technet.microsoft.com/en-us/library/security/ms17-010.aspx#ID0ERPAG)
* [A python2 script for sweeping a network to find windows systems compromised with the DOUBLEPULSAR implant.](https://github.com/countercept/doublepulsar-detection-script)
* [Backdoor.Doublepulsar - Removal](https://www.symantec.com/security_response/writeup.jsp?docid=2017-042122-0603-99&tabid=3)

> CVE-2017-0143, CVE-2017-0144, CVE-2017-0145, CVE-2017-0146, CVE-2017-0148
