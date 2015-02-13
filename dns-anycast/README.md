# Anycast lab 

Based in Vicent Bernat lab http://vincent.bernat.im/en/blog/2011-dns-anycast.html .

Core routers are IOL Linux.

DNS servers are Quagga Linux. 

PC users:

* Acquire IP by DHCP with network 192.168.X.0/24 where X is the PC number
* Route is announced in BGP

Quagga routers: 

* Loopback address 8.8.8.8/24
* They announce 8.8.8.8/24 prefix, simulating google anycast
* eth0 = 10.0.0.2 

IOL Routers:

* ID = 2 last digits of ASN ID=646XX
* Loopback0 = 1.1.1.XX
* Inter-routing addresses 10.ID1.ID2.0/24 and ID1 < ID2
* ID1 use .1 and ID2 use .2



![topology](https://github.com/itsuugo/gns3labs/blob/master/dns-anycast/screenshot.png)
 

