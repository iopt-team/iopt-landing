---
title: Cisco will not patch critical flaw CVE-2021-34730 in EoF routers
---
The issue resides in the router Universal Plug-and-Play (UPnP) service, enabling an unauthenticated, remote attacker to execute arbitrary code or cause an affected device to restart unexpectedly, resulting in a denial of service (DoS) condition.

This vulnerability is due to improper validation of incoming UPnP traffic. An attacker could exploit this vulnerability by sending a crafted UPnP request to an affected device. A successful exploit could allow the attacker to execute arbitrary code as the root user on the underlying operating system or cause the device to reload, resulting in a DoS condition.

This vulnerability affects the following Cisco Small Business RV Series Routers if they have UPnP configured:

* RV110W Wireless-N VPN Firewalls
* RV130 VPN Routers
* RV130W Wireless-N Multifunction VPN Routers
* RV215W Wireless-N VPN Routers

#### Recommendations

The UPnP service is enabled by default on LAN interfaces and disabled by default on WAN interfaces. If UPnP is disabled on both the LAN and WAN interfaces, the device is not considered vulnerable.

The vulnerability will not be patched, since the devices reached end-of-life in 2019.

To determine whether the UPnP feature is enabled on the LAN interface of a device, open the web-based management interface and navigate to Basic Settings > UPnP. If the Disable check box is unchecked, UPnP is enabled on the device.

There are no workarounds that address this vulnerability. However, administrators may disable UPnP on the LAN interface of a device.

#### References

* [Cisco Small Business RV110W, RV130, RV130W, and RV215W Routers Remote Command Execution and Denial of Service Vulnerability](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-cisco-sb-rv-overflow-htpymMB5)

> CVE-2021-34730
