# OSI 7-Layer Networking Model

## Layer 1: Physical

Physical medium to send and receive bit streams. No address is parsed.
Simultaneous transmissions create collisions. No collision detection. No device
to device communication.



## Layer 2: Data Link

Requires a functional layer 1. Uses a MAC address. Provides media control
access. Able to do unicast (1:1) and broadcast (1:all). Uses Ethernet protocol
(others include PPP, MPLS, ATM).

- Frame:
    - Preamble | dst MAC | src MAC | ET (EtherType Protocol) | Payload | Chksum
- CSMA/CD
    - Carrier-sense multiple access with collision detection.
    - If a collision is detected, a random backoff happens.


## Layer 3: Network

Does not provide channels of communications. Packets can be delivered out of
order. No flow control. Packets can be delayed or dropped.

### Internet Protocol (IP)

Has a network part (first 2 numbers) and host part (last 2 numbers).

- Packet Structure
    - v4
        - blah | ttl (time to live) | protocol | src IP | dst IP | data
    - v6
        - blah | hop limit | src IP (big) | dst IP (big) | data


### Subnet Mask
- 1 represents the network, 0 represents the host.
- 255.255.0.0 is the same as /16 prefix.


### Route Tables & Routes

The prefix /16 or /24 means how many 1 are in a subnet mask.  0 is the lowest,
32 is the highest. Each packet is forwarded to the `Next Hop/Target`


### Address Resolution Protocol (ARP)

Manages the relationship between IP address and MAC address.


### IP Routing

A router is a layer 3 device. It routes IP address to local or remote networks.


## Layer 4: Transport

Has TCP and UDP.

### TPC
- Transmission Control Protocol
- Slow
- Reliable

#### Encrypted by default
- tcp/443 HTTPS
- tcp/22 SSH
- tcp/3389 REMOTE DESKTOP PROTOCOL


#### Not encrypted by default
- tcp/80 HTTP
- tcp/25 SMTP (email)
- tcp/21 TELNET
- tcp/3306 MySQL/MariaDB/Aurora


#### TCP Segments

A channel is a collection of segments.

- header
    - src Port | dst Port | sequence number | ack | flags 'n' things | window | chksum | urgent pointer
- data


### UDP
- Fast
- Less reliable


### Stateless vs Stateful Firewall
- Stateless: out and in are separate rules.
- Stateful: out implicitly allows in.
