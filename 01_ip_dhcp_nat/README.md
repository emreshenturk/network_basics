# IP

IP has 4 groups. Each group contains 8 bits (1 byte). For example, in 192.168.1.101, a group can be at most 255, because the maximum value of 8 bits is 11111111.

Class A: 0.0.0.0 – 127.255.255.255
* The first 8 bits are for the network, and the rest are for hosts.
* Few networks, but many hosts.
* Used by governments and large technology companies.

Class B: 128.0.0.0 – 191.255.255.255
* The first 16 bits are for the network, and the rest are for hosts.
* It can contain 65,536 hosts.
* It is usually used by universities and medium–large companies.

Class C: 192.0.0.0 – 223.255.255.255
* The first 24 bits are for the network, and the rest are for hosts.
* Many networks but few hosts: 256 (254 usable) hosts.
* Used by houses or small businesses.

## Private and Public IPs
There are not enough public IPv4 addresses, so private IP addresses are reserved for LANs.
* 10.0.0.0 – 10.255.255.255: Used by large organizations to support many devices.
172.16.0.0 - 172.31.255.255: Middle range networks.
* 192.168.0.0 – 192.168.255.255: Used by homes and small businesses. If you run ifconfig in Kali, you may see these IP addresses.

## DHCP
* Request: When a host connects to a LAN, it sends a message saying “I want an IP address.”
* Assignment: The DHCP server assigns an IP address to the device.
* Lease: An IP address is given for a limited time.

DHCP infos:
* DHCP works on the seventh layer (Application layer) of the OSI model. It uses UDP ports 67 and 68.
* A DHCP server can assign 256 IP addresses, but only 254 are usable. 192.168.0.0 is the network address, 192.168.0.255 is the broadcast address.

## NAT
NAT (Network Address Translation) converts private IP addresses to public IP addresses. It keeps a table to track these mappings and always matches them when the device accesses the internet.

## ifconfig command in Kali
eth0:
* flags: The flags show the properties BROADCAST, RUNNING, and MULTICAST.
* mtu 1500: It stands for Maximum Transmission Unit; it indicates the largest size of data (in bytes) that can be sent in a single packet.
* innet: Out local ip address.
* netmask: It is the subnet mask.
* broadcast: The broadcast address used to send data to all devices on the network.
* inet6: The IPv6 address of the device.
* ether: The device’s MAC address; it is the unique physical identifier of the hardware.
* RX packets / TX packets: Statistics showing the number of received (RX) and transmitted (TX) packets, the amount of data, and any errors if present.

lo: 
* The IP address of this interface is always 127.0.0.1 (localhost). When you run a web server on your own machine, you access it through the lo interface.


