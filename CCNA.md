# CCNA


## OSI TCP/IP

![image alt](https://www.guru99.com/images/1/102219_1135_TCPIPvsOSIM1.png)
| OSI Model|TCP/IP Model|
| -------- | -------- |
|It is developed by ISO (International Standard Organization)|It is developed by ARPANET (Advanced Research Project Agency Network).|
|OSI model provides a clear distinction between interfaces, services, and protocols.|TCP/IP doesn't have any clear distinguishing points between services, interfaces, and protocols.|
|OSI refers to Open Systems Interconnection.|TCP refers to Transmission Control Protocol.|
|OSI uses the network layer to define routing standards and protocols.|TCP/IP uses only the Internet layer.|
|OSI follows a vertical approach.|TCP/IP follows a horizontal approach.|
|OSI layers have seven layers.|TCP/IP has four layers.|
|In the OSI model, the transport layer is only connection-oriented.|A layer of the TCP/IP model is both connection-oriented and connectionless.|
|In the OSI model, the data link layer and physical are separate layers.|In TCP, physical and data link are both combined as a single host-to-network layer.|
|Session and presentation layers are a part of the OSI model. |There is no session and presentation layer in the TCP model.|
|It is defined after the advent of the Internet.|It is defined before the advent of the internet.|
|The minimum size of the OSI header is 5 bytes.|The minimum header size is 20 bytes.|


## IP
### What is IP
Internet Protocol
a lable assigned to nodes that commected to a network that use internet protocol for communication with other nodes.
### IPV4
Internet Protocol Version 4,the fourth version of the internet protocol. It is one of the standards based networking methods in the internet networks.
#### Addressing
![image alt](https://upload.wikimedia.org/wikipedia/commons/7/74/Ipv4_address.svg)

![image alt](https://upload.wikimedia.org/wikipedia/commons/7/71/IPv4_Packet_-en.svg)
#### Class
|     |Class A|Class B|Class C|Class D|Class E|
| --- | --- | --- | -------- | -------- | -------- |
|IP Range|1.0.0.0~127.255.255.255|128.0.0.0~191.255.255.255|192.0.0.0~223.255.255.255|224.0.0.0~239.255.255.255|240.0.0.0~255.255.255.255|
|Available IP Range |1.0.0.1~127.255.255.254|128.0.0.1~191.255.255.254|192.0.0.1~223.255.255.254 |          |          |
|Can be assigned to the host |YES|YES|YES|NO|NO|
|IP amount|126 (27-2)|16384 (214)|2097152 (221)|          |          |
|Host amount|16777214 (224-2)|65534 (216-2)|254 (28-2)|          |          |
|applicable|Large Network with a Large amount of hosts|Network with medium sized hosts|Small local area network|Use by the Internet Architecture Board (IAB) Multicast address|only of research,Internet experimet and development|
#### Special Use Address
|Address Book|Address Reange|Number Of Addresses|Scope|Description|
| --- | --- | -------- | -------- | -------- |
|0.0.0.0/8|0.0.0.0–0.255.255.255|16777216|Software|Current network (only valid as source address). |
|10.0.0.0/8|10.0.0.0–10.255.255.255|16777216|Private network|Used for local communications within a private network.|
|100.64.0.0/10|100.64.0.0–100.127.255.255|4194304|Private network|Shared address space for communications between a service provider and its subscribers when using a carrier-grade NAT. |
|127.0.0.0/8|127.0.0.0–127.255.255.255|16777216|Host|Used for loopback addresses to the local host.|
|169.254.0.0/16|169.254.0.0–169.254.255.255|65536|Subnet|Used for link-local addresses between two hosts on a single link when no IP address is otherwise specified, such as would have normally been retrieved from a DHCP server. |
|172.16.0.0/12|172.16.0.0–172.31.255.255|1048576 |Private network|Used for local communications within a private network.|
|192.0.0.0/24|192.0.0.0–192.0.0.255|256|Private network|IETF Protocol Assignments.|
|192.0.2.0/24|192.0.2.0–192.0.2.255|256|Documentation|Assigned as TEST-NET-1, documentation and examples.|
|192.88.99.0/24|192.88.99.0–192.88.99.255|256|Internet|Reserved. Formerly used for IPv6 to IPv4 relay (included IPv6 address block 2002::/16). |
|192.168.0.0/16|192.168.0.0–192.168.255.255|65536|Private network|Used for local communications within a private network.|
|198.18.0.0/15|198.18.0.0–198.19.255.255|131072|Private network|Used for benchmark testing of inter-network communications between two separate subnets.|
|198.51.100.0/24|198.51.100.0–198.51.100.255|256|Documentation|Assigned as TEST-NET-2, documentation and examples.|
|203.0.113.0/24|203.0.113.0–203.0.113.255|256|Documentation|Assigned as TEST-NET-3, documentation and examples.|
|224.0.0.0/4|224.0.0.0–239.255.255.255|268435455|Internet|In use for IP multicast. (Former Class D network). |
|240.0.0.0/4|240.0.0.0–255.255.255.254|268435455|Internet|Reserved for future use. (Former Class E network). |
|255.255.255.255/32|255.255.255.255|1|Subnet|Reserved for the "limited broadcast" destination address.|

#### Loopback
The class A network 127.0.0.0 (classless network 127.0.0.0/8) is reserved for loopback. IP packets whose source addresses belong to this network should never appear outside a host. Packets received on a non-loopback interface with a loopback source or destination address must be dropped. 

#### First and last subnet addresses
The first address in a subnet is used to identify the subnet itself. In this address all host bits are 0. To avoid ambiguity in representation, this address is reserved. The last address has all host bits set to 1. It is used as a local broadcast address for sending messages to all devices on the subnet simultaneously. For networks of size /24 or larger, the broadcast address always ends in 255.

#### Example
192.168.5.0/24
||Binary Form|Dot-decimal notation|
| -------- | -------- | -------- |
|Network space|11000000.10101000.00000101.<font color=red>00000000</font>|192.168.5.<font color=red>0</font> |
|Broadcast address|11000000.10101000.00000101.<font color=red>11111111</font>|192.168.5.<font color=red>255</font> |

192.168.0.1/28
||Binary Form|Dot-decimal notation|
| -------- | -------- | -------- |
|Network space|11000000.10101000.00000000.0000<font color=red>0000</font>|192.168.0.<font color=red>0</font> |
|Broadcast address|11000000.10101000.00000000.0000<font color=red>1111</font>|192.168.0.<font color=red>15</font> |


10.0.0.1/16
||Binary Form|Dot-decimal notation|
| -------- | -------- | -------- |
|Network space|00001010.00000000.<font color=red>00000000.00000000</font>|10.0.<font color=red>0.0</font> |
|Broadcast address|00001010.00000000.<font color=red>11111111.11111111</font>|10.0.<font color=red>255.255</font> |

100.200.0.1/12
||Binary Form|Dot-decimal notation|
| -------- | -------- | -------- |
|Network space|01101000.11<font color=red>000000.00000000.00000000</font>|100.192.<font color=red>0.0</font> |
|Broadcast address|01101000.11<font color=red>001111.11111111.11111111</font>|100.207.<font color=red>255.255</font> |
### IPV6 
