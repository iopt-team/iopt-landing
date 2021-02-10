The rom-0 backup file contains sensitive information such as the router password. There is a disclosure in which anyone can download the file without any authentication. Vulnerability is easily identifiable by querying /rom-0 via HTTP GET request. Affected devices include ZTE, TP-Link, ZynOS, Huawei and many others.

#### Recommendations

Most of the vendors issued patch for their routers, but still there are many routers out there where patch is not available. Mitigation would be to firewall HTTP from WAN side.

#### References

* [ZTE, TP-Link, ZynOS, Huawei rom-0 Configuration Decompressor](https://packetstormsecurity.com/files/127049/ZTE-TP-Link-ZynOS-Huawei-rom-0-Configuration-Decompressor.html)
* [HOW I SAVED YOUR A** FROM THE ZYNOS (ROM-0) ATTACK !!](https://nasro.me/2014/01/11/how-i-saved-your-a-from-the-zynos-rom-0-attack-full-disclosure/)

> CVE-2014-4019
