---
title: An unauthenticated network-adjacent RCE by abusing the tldServer daemon
---
Vulnerability allows network-adjacent attackers to execute arbitrary code on affected installations of TP-Link Archer A7 Firmware Ver: 190726 AC1750 routers. Authentication 
is not required to exploit this vulnerability. The specific flaw exists within the tdpServer service, which listens on UDP port 20002 by default. When parsing the slave_mac 
parameter, the process does not properly validate a user-supplied string before using it to execute a system call. An attacker can leverage this vulnerability to execute code 
in the context of the root user.

#### Recommendations
	
Fixed in version A7(US)_V5_200220

#### References

- [https://www.zerodayinitiative.com/advisories/ZDI-20-334/](https://www.zerodayinitiative.com/advisories/ZDI-20-334)
- [https://packetstormsecurity.com/files/157255/TP-Link-Archer-A7-C7-Unauthenticated-LAN-Remote-Code-Execution.html](https://packetstormsecurity.com/files/157255/TP-Link-Archer-A7-C7-Unauthenticated-LAN-Remote-Code-Execution.html)

> CVE-2020-10882
