A vulnerability allows network-adjacent attackers to execute arbitrary code on affected installations of NETGEAR R7000 routers. Authentication is not required to exploit this vulnerability. The vulnerability exists within the handling of HTTP request, the issue results from the lack of proper validation of user supplied data, which can result a heap overflow. An attacker can leverage this vulnerability to execute code with the root privilege.

#### Recommendations

It is strongly recommended that you download the latest firmware as soon ASAP.

#### References

- [SSD Advisory – NETGEAR Nighthawk R7000 httpd PreAuth RCE](https://ssd-disclosure.com/ssd-advisory-netgear-nighthawk-r7000-httpd-preauth-rce/)

> CVE-2021-31802
