## About IoPT

**IoPT** is abbreviated from *"Internet of Protected Things"*. The aim of **IoPT** is to check SoHo(small office/home office) network security state by searching for a vulnerable network connected device(s). By using **IoPT**, you will get know, what security issue(s) do you have and how to fix it.

**IMPORTANT: PLEASE READ THE [LICENSE](eula.md) CAREFULLY BEFORE USING THIS SOFTWARE.**

### Key Features

- Security audit - Identify services on a network and perform the security audit
- Host discovery - Identify hosts on a network
- Port scanning - Enumerate the open TCP ports on a target host
- HiBP integration - Ensure your personal data has not been compromised by data breaches
- Shodan integration - Ensure you know all the "things" on a network directly connected to the Internet
- RTSP audit - Perform a security audit for an RTSP source(e.g. CCTV installation). Check your network for unauthorized CCTV installations.

### Vulnerability Tests

- [*CVE–2014–9222* aka "Misfortune Cookie" vulerability](vulndb/allegrosoft-rompager-4-34-and-earlier-allows-remote-attackers-to-gain-privileges.md)
- [*CVE-2014-4019* the rom-0 backup file](vulndb/rom-0-backup-file-disclosure.md)
- [*CVE-2014-9583* unauthenticated command execution vulnerability in ASUS "infosrv" UDP service](vulndb/unauthenticated-command-execution-vulnerability-in-asus-infosrv-udp-service.md)
- [Linksys E-Series unauthenticated OS command injection](vulndb/some-linksys-e-series-routers-are-vulnerable-to-an-unauthenticated-os-command-injection.md)
- [DBL(Domain Name System Blacklists) enlisting](vulndb/about-dnsbl.md)
- [*CVE-2020-12695* SSRF-like vulnerability detected a.k.a. CallStranger](vulndb/ssrf-like-vuln-aka-callstranger.md)
- [Check if DNS server IP address and the network public IP address belong to the same GEO and/or ISP](vulndb/is-the-rogue-dns-server-so-dangerous.md)
- [*CVE-2017-0144* SMB server allows remote attackers to execute arbitrary code via crafted packets](vulndb/multiple-windows-smb-remote-code-execution-vulnerabilities.md)
- [MikroTik RouterOS contains a remote code execution vulnerability aka "Chimay Red"](vulndb/a-remote-code-execution-vulnerability-aka-chimay-red-exists-in-mikrotik-routeros-versions-prior-to-6-38-5.md)
- [*CVE-2017-5135* SNMP authentication bypass(aka StringBleed)](vulndb/snmp-authentication-bypass-vulnerability-aka-stringbleed.md)
- [*CVE-2019-7192,CVE-2019-7194,CVE-2019-7195* A local file inclusion vulnerability that allows an unauthenticated attacker to download files from the QNAP filesystem](vulndb/several-vulnerabilities-affect-multiple-versions-of-qts-and-photo-station.md)
- [*CVE-2020-11117* An exploitable command execution vulnerability in the lbd service functionality of Qualcomm](vulndb/synology-srm-lbd-service-command-execution-vulnerability.md)
- [An unauthenticated PHP code injection in Seagate NAS products](vulndb/seagate-nas-unauthenticated-rce-via-php-injection.md)
- [*CVE-2020-27403* A vulnerability in the TCL Android Smart TV series by TCL Technology Group Corporation](vulndb/vulnerabilities-found-in-tcl-android-tvs.md)
- [*CVE-2020-10882* An unauthenticated network-adjacent RCE by abusing the tldServer daemon](vulndb/tp-link-archer-a7-c7-unauthenticated-lan-rce.md)
- [*CVE-2020-28184* XSS in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28185* User enumeration in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28186* Email injection in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28187* Directory traversal in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28188* Unauthenticated remote command execution in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28189* Incorrect access control in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [*CVE-2020-28190* Software update via insecure communication channel in TerraMaster TOS <= 4.2.06](vulndb/multiple-vulnerabilities-in-terramaster-tos-lt-4206.md)
- [Netgear httpd upgrade_check.cgi stack buffer overflow](vulndb/pre-authentication-rce-in-netgear-soho-devices.md)

### Toolset

- **"Have I Been Pwned tool"** - Allows to check, if you have an account that has been compromised in a data breach
- **"Shodan visibility tool"** - Allows to check, if you have someting exposed directly to the Internet
- **"Port scanning tool"** - Allows to check, which port(s) is open on a remote device
- **"RTSP audit"** - Allows to check, if you have CCTV installation security issues or find unauthorized CCTV installations
