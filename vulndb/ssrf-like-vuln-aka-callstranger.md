---
title: SSRF-like vulnerability detected a.k.a. CallStranger
---
The CallStranger vulnerability that is found in billions of UPNP devices can be used to exfiltrate data (even if you have proper DLP/border security means) or scan 
your network or even cause your network to participate in a DDoS attack.

The vulnerability – CallStranger – is caused by Callback header value in UPnP SUBSCRIBE function can be controlled by an attacker and enables an SSRF-like vulnerability 
which affects millions of Internet facing and billions of LAN devices. This vulnerability can used for:

- Bypassing DLP and network security devices to exfiltrate data
- Using millions of Internet-facing UPnP device as source of amplified reflected TCP DDoS
- Scanning internal ports from Internet facing UPnP devices

Because this is a protocol vulnerability, it may take a long time for vendors to provide patches.

#### Recommendations

Home users are not expected to be targeted directly. If their internet facing devices have UPnP endpoints, their devices may be used for DDoS source. 
Ask your ISP if your router has Internet facing UPnP with CallStranger vulnerability -there are millions of consumer devices exposed to Internet. 
Don't port forward to UPnP endpoints. Home users don't need to disable UPnP for this vulnerability. They just need to be sure UPnP endpoint is not exposed to Internet.

#### References

* [http://callstranger.com/](http://callstranger.com/)
* [CallStranger - Technical Report.pdf](</files/CallStranger - Technical Report.pdf>)

> CVE-2020-12695
