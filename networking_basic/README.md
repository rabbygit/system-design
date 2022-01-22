#### NAT:
It stands for Network Address Translation.To access the Internet, one public IP address is needed, but we can use a private IP address in our private network. The idea of NAT is to allow multiple devices to access the Internet through a single public address. To achieve this, the translation of a private IP address to a public IP address is required. Network Address Translation (NAT) is a process in which one or more local IP address is translated into one or more Global IP address and vice versa in order to provide Internet access to the local hosts. Also, it does the translation of port numbers i.e. masks the port number of the host with another port number, in the packet that will be routed to the destination. It then makes the corresponding entries of IP address and port number in the NAT table.

![NAT](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/NAT_Concept-en.svg/1024px-NAT_Concept-en.svg.png)

#### Latency:
Network latency is the amount of time it takes for a data packet to go from one place to another.Latency is measured in milliseconds, or during speed tests, it’s referred to as a ping rate. When delays in transmission are small, it’s referred to as a low-latency network (desirable) and longer delays are called a high-latency network (not so desirable).

#### DTR:
The data transfer rate (DTR) is the amount of digital data that is moved from one place to another in a given time. The data transfer rate can be viewed as the speed of travel of a given amount of data from one place to another.In telecommunications, data transfer is usually measured in bits per second. For example, a typical low-speed connection to the Internet may be 33.6 kilobits per second (Kbps).

#### Bandwidth:
Bandwidth is measured as the amount of data that can be transferred from one point to another within a network in a specific amount of time.

#### TCP:
The Transmission Control Protocol (TCP) is one of the main protocols of the Internet protocol suite.TCP is connection-oriented, and a connection between client and server is established before data can be sent. TCP is reliable because the protocol ensures that all data is fully transmitted and can be assembled by the receiver in the correct order.TCP is positioned at the transport layer (layer 4) of the OSI model.

![TCP](https://www.ionos.com/digitalguide/fileadmin/DigitalGuide/Schaubilder/EN-tcp.png)

#### UDP:
In computer networking, the User Datagram Protocol (UDP) is one of the core members of the Internet protocol suite. With UDP, computer applications can send messages, in this case referred to as datagrams, to other hosts on an Internet Protocol (IP) network. Prior communications are not required in order to set up communication channels or data paths.

UDP uses a simple connectionless communication model with a minimum of protocol mechanisms. UDP provides checksums for data integrity, and port numbers for addressing different functions at the source and destination of the datagram. It has no handshaking dialogues, and thus exposes the user's program to any unreliability of the underlying network; there is no guarantee of delivery, ordering, or duplicate protection. If error-correction facilities are needed at the network interface level, an application may use Transmission Control Protocol (TCP) or Stream Control Transmission Protocol (SCTP) which are designed for this purpose.

UDP is commonly used in time-sensitive communications where occasionally dropping packets is better than waiting. Voice and video traffic are sent using this protocol because they are both time-sensitive and designed to handle some level of loss. For example VOIP (voice over IP), which is used by many internet-based telephone services, operates over UDP. This is because a staticy phone conversation is preferable to one that is crystal clear but heavily delayed.

This also makes UDP the ideal protocol for online gaming. Similarly, because DNS servers both need to be fast and efficient, they operate though UDP as well.

![UDP](https://www.cloudflare.com/img/learning/ddos/glossary/user-datagram-protocol-udp/tcp-vs-udp.svg)

#### Ring Buffer:
A ring is a circular buffer where packets for rx(receives)/tx(transmits) are stored. More specifically, each slot in the ring contains the length and physical address of a packet buffer. CPU-accessible registers in the NIC indicate the portion of the ring available for transmission or reception. 

When a packet arrives, the NIC does a DMA to store the packet in the address pointed to by the RX ring, updates the ring with this information that the packet has been copied, and raises an interrupt to the kernel. Until the kernel (device driver) comes around to servicing the interrupt, further interrupts from the NIC are disabled. The interrupts are reenabled once the kernel services the interrupt from this device. The kernel only does minimal procesing in the interrupt service routine / hardware interrupt handler, and schedules a kernel thread (softirq) to perform the rest of the TCP/IP processing (bottom half of the interrupt service routine). The bottom half / softirq removes the buffers from the ring for network stack processing, and reinitializes the ring with new buffers. After TCP/IP processing, the packet buffers are queued up at the receive socket buffer. When the user program calls read, the payload is copied from the kernel buffers to userspace memory, and the kernel buffer is freed. New connections (after completion of 3-way TCP handshake) are queued up in the backlog queue and can be accessed via accept. 

![RING_BUFFER](https://i.stack.imgur.com/BKBvW.png)

#### CIDR:
Classless inter-domain routing (CIDR) is a set of Internet protocol (IP) standards that is used to create unique identifiers for networks and individual devices. The IP addresses allow particular information packets to be sent to specific computers. Shortly after the introduction of CIDR, technicians found it difficult to track and label IP addresses, so a notation system was developed to make the process more efficient and standardized. That system is known as CIDR notation. 

![CIDR](https://whatismyipaddress.com/wp-content/uploads/cidr-notation.png)

#### DHCP:
A DHCP Server is a network server that automatically provides and assigns IP addresses, default gateways and other network parameters to client devices. It relies on the standard protocol known as Dynamic Host Configuration Protocol or DHCP to respond to broadcast queries by clients.

A DHCP server automatically sends the required network parameters for clients to properly communicate on the network. Without it, the network administrator has to manually set up every client that joins the network, which can be cumbersome, especially in large networks. DHCP servers usually assign each client with a unique dynamic IP address, which changes when the client’s lease for that IP address has expired.

![DHCP](https://upload.wikimedia.org/wikipedia/commons/e/e4/DHCP_session.svg)

