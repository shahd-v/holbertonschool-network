# Networking basics #0

## Files

- `0-OSI_model`: conceptual OSI model; layers ordered from lowest to highest.
- `1-types_of_network`: LAN, WAN, and Internet answers.
- `2-MAC_and_IP_address`: MAC identifies an interface; IP provides its network address.
- `3-UDP_and_TCP`: TCP provides reliable, ordered delivery; UDP does not guarantee delivery or order. TCP acknowledges receipt.
- `4-TCP_and_UDP_ports`: displays listening sockets, process IDs, and program names using `netstat -lp`. Run with sudo to see processes owned by other users.
- `5-is_the_host_on_the_network`: sends five ICMP echo requests to the supplied address; prints usage when no argument is supplied.

## Concepts

The seven OSI layers, lowest to highest, are Physical, Data Link, Network,
Transport, Session, Presentation, and Application. OSI is a conceptual framework.

A LAN connects nearby devices in a home, office, or campus. A WAN connects
networks over larger distances, including between offices, cities, and countries.
The Internet is the global network of interconnected networks using IP.

An IP address identifies an interface for network communication. Public addresses
are globally routable; private addresses are used within private networks.
IPv4 uses 32-bit addresses and IPv6 uses 128-bit addresses. IPv6 was created
primarily to address IPv4 address exhaustion. A subnet is a logical IP network
identified by a shared network prefix. Localhost refers to the current machine,
commonly using 127.0.0.1 for IPv4 or ::1 for IPv6.

TCP and UDP operate at the transport layer. TCP establishes connections and uses
acknowledgments, retransmission, and ordering. UDP sends datagrams with less
overhead, without those guarantees. Actual speed depends on the application and
network conditions.

A port identifies a transport endpoint used by a service: SSH uses 22, HTTP uses
80, and HTTPS uses 443. The ping utility uses ICMP echo requests and replies to
test reachability. A missing reply can also result from filtering.

## Usage on Ubuntu 22.04

Install net-tools and iputils-ping if necessary, then run:

```sh
sudo ./4-TCP_and_UDP_ports
./5-is_the_host_on_the_network 127.0.0.1
```
