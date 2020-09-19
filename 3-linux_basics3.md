# Linux Basics 3

## Today 13 Sep 2020

- This course does not cover networking skills, but are essential for hacking. Obviously!
- `ifconfig` command shows a lot of network information on a system. Try it and learn it separately.
- `ping` command tries to talk to another device which is on the internet or intranet.
- `arp` commands associates mac address with IP address `arp -a`
- `netstat -ano` command shows you all the ports on this system that are open, and what's connected to them.
- `route` command shows the routing table; you need to google and learn this separately, because this is very vast topic to cover here in this note. For example, check this [link](https://www.youtube.com/watch?v=g8eP4fhrx3I).


**Something that cannot go into any of these notes is `history` command, which shows you all the commands you ran in the present session.**

### More on `route` command:

- First of all, I did not see much when I tried this command on the Kali VM I am running through this course.
- Cyber Mentor said that it would give some interesting information if you had some nice network going on. I thought lets try then on our local PC, which is obviously wired on a network which is again connected to multiple devices, starting from a router to a set top box, several wireless devices, mobiles and smart TVs. On Windows, it needs additional flag, so I tried the following command on Windows PC I am using and below is its output.

```
C:\Users\Dell Optiplex>route print
===========================================================================
Interface List
  6...90 b1 1c 9f 37 13 ......Intel(R) 82579LM Gigabit Network Connection
 15...74 ee 2a fb 64 70 ......Microsoft Wi-Fi Direct Virtual Adapter
  3...74 ee 2a fb 64 71 ......Microsoft Wi-Fi Direct Virtual Adapter #2
 12...00 50 56 c0 00 01 ......VMware Virtual Ethernet Adapter for VMnet1
 17...00 50 56 c0 00 08 ......VMware Virtual Ethernet Adapter for VMnet8
 16...74 ee 2a fb 64 76 ......802.11n USB Wireless LAN Card
  1...........................Software Loopback Interface 1
===========================================================================

IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
          0.0.0.0          0.0.0.0      192.168.1.1    192.168.1.100     25
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    331
        127.0.0.1  255.255.255.255         On-link         127.0.0.1    331
  127.255.255.255  255.255.255.255         On-link         127.0.0.1    331
      192.168.1.0    255.255.255.0         On-link     192.168.1.100    281
    192.168.1.100  255.255.255.255         On-link     192.168.1.100    281
    192.168.1.255  255.255.255.255         On-link     192.168.1.100    281
    192.168.164.0    255.255.255.0         On-link     192.168.164.1    291
    192.168.164.1  255.255.255.255         On-link     192.168.164.1    291
  192.168.164.255  255.255.255.255         On-link     192.168.164.1    291
    192.168.194.0    255.255.255.0         On-link     192.168.194.1    291
    192.168.194.1  255.255.255.255         On-link     192.168.194.1    291
  192.168.194.255  255.255.255.255         On-link     192.168.194.1    291
        224.0.0.0        240.0.0.0         On-link         127.0.0.1    331
        224.0.0.0        240.0.0.0         On-link     192.168.194.1    291
        224.0.0.0        240.0.0.0         On-link     192.168.164.1    291
        224.0.0.0        240.0.0.0         On-link     192.168.1.100    281
  255.255.255.255  255.255.255.255         On-link         127.0.0.1    331
  255.255.255.255  255.255.255.255         On-link     192.168.194.1    291
  255.255.255.255  255.255.255.255         On-link     192.168.164.1    291
  255.255.255.255  255.255.255.255         On-link     192.168.1.100    281
===========================================================================
Persistent Routes:
  None

IPv6 Route Table
===========================================================================
Active Routes:
 If Metric Network Destination      Gateway
  6    281 ::/0                     fe80::429b:cdff:fe3e:1d8c
  1    331 ::1/128                  On-link
  6    281 2001:8f8:1629:2ae2::/64  On-link
  6    281 2001:8f8:1629:2ae2:6084:b7fa:9bf:9385/128
                                    On-link
  6    281 2001:8f8:1629:2ae2:65c2:2b97:6d15:67fe/128
                                    On-link
 12    291 fe80::/64                On-link
 17    291 fe80::/64                On-link
  6    281 fe80::/64                On-link
  6    281 fe80::65c2:2b97:6d15:67fe/128
                                    On-link
 17    291 fe80::e881:3d01:bb7c:f6fe/128
                                    On-link
 12    291 fe80::ec62:6b4d:933a:2250/128
                                    On-link
  1    331 ff00::/8                 On-link
 12    291 ff00::/8                 On-link
 17    291 ff00::/8                 On-link
  6    281 ff00::/8                 On-link
===========================================================================
Persistent Routes:
  None
```
