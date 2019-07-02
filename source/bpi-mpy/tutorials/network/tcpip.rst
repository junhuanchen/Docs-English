Introduction to TCP/IP
================

*Reprinted to * `[廖雪峰Python Tutorial] <https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014320037768360d53e4e935ca4a1f96eed1c896ad1217000>`_



Although everyone is familiar with the Internet now, the emergence of computer networks is much earlier than the Internet.

In order to connect to the Internet, computers must stipulate communication protocols. In the early days of computer networks, each vendor specified a set of protocols. IBM, Apple, and Microsoft all had their own network protocols, which were incompatible with each other. This is like a group of people saying that English, some speak Chinese, some speak German, people who speak the same language can communicate, and different languages ​​can't.

In order to connect all the different types of computers around the world, a set of global protocols must be defined. In order to achieve the Internet, the Internet Protocol Suite is a common protocol standard. The Internet is a combination of two words, inter and net. The original intention is to connect to the "network" network. With the Internet, any private network can connect to the Internet as long as it supports this protocol.

Because the Internet Protocol contains hundreds of protocol standards, the two most important ones are TCP and IP protocols. Therefore, the Internet protocol is referred to as the TCP/IP protocol.

When communicating, both parties must know each other's logo, just like sending an email must know the other party's email address. The unique identifier for each computer on the Internet is the IP address, similar to ``123.123.123.123``. If a computer accesses two or more networks at the same time, such as a router, it will have two or more IP addresses. Therefore, the IP address corresponds to the computer's network interface, usually a network card.

The IP protocol is responsible for sending data from one computer to another via the network. The data is divided into small pieces and then sent out through IP packets. Due to the complexity of the Internet link, there are often multiple lines between the two computers, so the router is responsible for deciding how to forward an IP packet. The characteristics of an IP packet are that it is sent in blocks, and multiple routes are routed, but it is not guaranteed to arrive, nor is it guaranteed to arrive in sequence.

.. image:: ../../images/tutorials/tcpip.png

The IP address is actually a 32-bit integer (called IPv4). The IP address represented by a string such as 192.168.0.1 is actually a digital representation of a 32-bit integer grouped by 8 bits for the purpose of reading.

The IPv6 address is actually a 128-bit integer, which is an upgraded version of IPv4 currently in use, represented by a string similar to ``2001:0db8:85a3:0042:1000:8a2e:0370:7334``.

The TCP protocol is built on top of the IP protocol. The TCP protocol is responsible for establishing a reliable connection between the two computers to ensure that the packets arrive in order. The TCP protocol establishes a connection by handshake, and then numbers each IP packet to ensure that the other party receives it in order. If the packet is lost, it is automatically resent.

Many commonly used higher-level protocols are based on the TCP protocol, such as the HTTP protocol for browsers, the SMTP protocol for sending mail, and so on.

In addition to the data to be transmitted, a TCP packet contains the source IP address and the destination IP address, the source port and the destination port.

What is the role of the port? When communicating between two computers, it is not enough to send only the IP address because there are multiple network programs running on the same computer. After a TCP message arrives, whether it is handed to the browser or QQ, the port number is required to distinguish. Each network program requests a unique port number from the operating system, so that two processes need their respective IP addresses and their respective port numbers to establish a network connection between the two computers.



Understand the basic concepts of TCP/IP, the concept of IP address and port, I can start network programming.