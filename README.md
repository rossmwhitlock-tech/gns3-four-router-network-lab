#Two-LAN Routing Lab with GNS3

This project demonstrates a manually configured two-LAN network in GNS3 using Alpine Linux hosts and routers, static IPv4 addressing, a /30 router-to-router transit network, and end-to-end routing verified with ping and traceroute.

## Skills Demonstrated

- TCP/IP addressing and subnetting

- Static routing between multiple IPv4 subnets

- Linux network configuration and troubleshooting

- Routing-table analysis using `ip route` and `ip route get`

- ARP and neighbor-table analysis using `ip neigh`

- Packet-path verification using `ping` and `traceroute`

- Packet inspection with Wireshark

- Ethernet switching, MAC addressing, and local Layer 2 forwarding

- Basic NAT, default gateway, and multi-hop routing concepts

## Network Topology

The lab contains two separate IPv4 LANs connected by two Linux routers. The routers communicate across a dedicated /30 transit network, and static routes allow hosts on each LAN to reach the other LAN.

```text
AlpinePC-1 (192.168.1.10/24)        
	|
     Switch1
	|
     Router1
  eth0: 192.168.1.1/24
  eth2: 10.0.12.1/30
        |
   10.0.12.0/30
        |
     Router2
eth1: 10.0.12.2/30
eth0: 192.168.2.1/24
	|
     Switch2
	|
AlpinePC-4 (192.168.2.10/24)


```text
