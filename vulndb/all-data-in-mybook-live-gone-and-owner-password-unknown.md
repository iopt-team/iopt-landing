On June 24th, 2021 Western Digital My Book Live device owners were finding that their storage partitions were being wiped clean, meaning years of data some users have collected over time (home videos and pictures, etc.) were inexplicably gone.

My Book Live devices are being mass exploited to join a botnet. One user seems to confirm this is the case, after they ran the payload through VirusTotal, which reported it was part of the Linux.Ngioweb malware family. It appears the actor(s) are taking advantage of CVE-2018-18472. The vulnerability allows simple unauthenticated remote command execution via a simple PUT request to the /api/1.0/rest/language_configuration endpoint.

However, this would not explain why there were reports of users claiming their partitions were wiped, and the logs about factoryRestore.sh running on user devices. [Censys](https://censys.io/blog/cve-2018-18472-western-digital-my-book-live-mass-exploitation/) disassembled the last available firmware from Western Digital for My Book Live to view the filesystem of these devices. There appears to be an unauthenticated zero-day vulnerability(CVE-2021-35941) with an endpoint aptly named system_factory_restore. This PHP REST endpoint has authentication code commented out (disabled) at the top (yes, this is in the latest shipping firmware, which was from 2015 as these devices are no longer supported by Western Digital). A simple POST request to the system_factory_restore endpoint would trigger the factory restore process.

#### Recommendations

Immediately disconnect your My Book Live and My Book Live Duo from the Internet to protect your data from ongoing attacks.

For customers who have lost data as a result of these attacks, Western Digital will provide data recovery services. My Book Live users will also be offered a trade-in program to upgrade to a supported My Cloud device. Both programs will be available beginning in July, and details on how to take advantage of these programs will be made available in a separate announcement.

#### References

* [Help! All data in mybook live gone and owner password unknown](https://community.wd.com/t/help-all-data-in-mybook-live-gone-and-owner-password-unknown/268111)
* [CVE-2018-18472: Western Digital My Book Live Mass Exploitation](https://censys.io/blog/cve-2018-18472-western-digital-my-book-live-mass-exploitation/9)
* [Recommended Security Measures for WD My Book Live and WD My Book Live Duo](https://www.westerndigital.com/support/productsecurity/wdc-21008-recommended-security-measures-wd-mybooklive-wd-mybookliveduo)
* [WizCase Report: Vulnerabilities found on WD My Book, NetGear Stora, SeaGate Home, Medion LifeCloud NAS](https://www.wizcase.com/blog/hack-2018/)

> CVE-2018-18472, CVE-2021-35941
