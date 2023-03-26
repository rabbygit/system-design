#### Host:
Host is a machine which can send or receive traffic. It can be computer,laptop,mobile etc.

![Host Image](https://cdn.ttgtmedia.com/rms/onlineImages/networking-network_and_host_ids_mobile.jpg)

#### IP Address:
It is the identity of a host.When client host initiates a request,it attaches it's ip address as source ip address and destination ip address to the data packet.
IP address is 32 bit and it is represeneted as four octetes(each octete is 8 bit).
*Example:172.22.22.33*

#### Network:
A network consits of two or more computers that are linked to each other in order to exchange resources.When a network consits a network,,it is called sub-nets.

#### Repeater:
In telecommunications, a repeater is an electronic device that receives a signal and retransmits/re-generates it. Repeaters are used to extend transmissions so that the signal can cover longer distances or be received on the other side of an obstruction.

<img width="898" alt="image" src="https://user-images.githubusercontent.com/39536118/227763131-8c80dc00-84ef-404f-a9ec-c4dc0e8fb2ca.png">

![Repeater image](https://www.tutorialsweb.com/images/networking-images/repeater.jpg)

#### Hub:
It is basically a multiport repeater and used to connect multiple devices in a network. One important note is hub can not filter data so data packets are sent to all connected devices and don't have the intillegence to find out the best path for data packets.

<img width="942" alt="image" src="https://user-images.githubusercontent.com/39536118/227763275-97a1de54-a060-4aaf-95b8-4bef2bae4f51.png">

#### Bridge:
Bridge sits between Hub connected hosts. It has only two ports and can filter contents. It can take decision to allow the data packets to travel to other side of the bridge.

<img width="915" alt="image" src="https://user-images.githubusercontent.com/39536118/227763350-616c8a12-2b1d-4257-97bd-1192cb58d737.png">

#### Switches:
It facilities communication *within* a network which is a combination of hub and bridge. It has multiple port repeater and also can filter conetents.

<img width="897" alt="image" src="https://user-images.githubusercontent.com/39536118/227763796-c8b5fb94-cf9f-4bcd-8978-c8b59457d0bd.png">

#### Routers:
It facilities communiacation *between* networks. It knows which networks they are connected to, stroed in routing tables.

<img width="911" alt="image" src="https://user-images.githubusercontent.com/39536118/227764008-6b384c8d-d672-4c44-8903-c214d62b742f.png">

The router basically performs two major functions: 
##### Forwarding – 
The router receives the packets from its input ports, checks its header, performs some basic functions like checking checksum, and then looks up to the routing table to find the appropriate output port to dump the packets onto, and forwards the packets onto that output port.
##### Routing – 
Routing is the process by which the router ascertains what is the best path for the packet to reach the destination, It maintains a routing table which is made using different algorithms by the router only.
![router](https://i.ytimg.com/vi/ZvWn5xBflUs/maxresdefault.jpg)

Summary:

<img width="894" alt="image" src="https://user-images.githubusercontent.com/39536118/227764137-7f17d1f0-825f-4a9e-87dd-85814add6e02.png">

#### MAC address:
A media access control address (MAC address) is a unique identifier assigned to a network interface controller (NIC) for use as a network address in communications within a network segment. MAC addresses are used in the media access protocol of the data link layer.MAC addresses are primarily assigned by device manufacturers, and are therefore often referred to as the burned-in address, or as an Ethernet hardware address, hardware address, or physical address.

![MAC](https://upload.wikimedia.org/wikipedia/commons/7/77/UMTS_Router_Surf%40home_II%2C_o2-0017.jpg)

#### NIC:
A network interface controller  is a computer hardware component that connects a computer to a computer network. it is also known as as a network interface card, network adapter, LAN adapter or physical network interface.

![NIC](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Network_card.jpg/1280px-Network_card.jpg)
