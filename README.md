# Lab 3 - SLAAC (Stateless Address Auto Configuration)

## Objective

Configure SLAAC and observe how a host automatically receives IPv6 addressing information through Router Advertisements (RA).

## Topology

PC1 -------- R1

## Configuration

### Router

```bash
ipv6 unicast-routing

interface g0/0
 ipv6 address 2001:DB8:1:1::1/64
 no shutdown
```

### PC

Desktop → IP Configuration

Select:

IPv6 Auto Config

## Verification Commands

### Router

```bash
show ipv6 interface brief
show ipv6 neighbors
```

### PC

```bash
ipconfig
ping 2001:DB8:1:1::1
```

## Concepts Learned

- SLAAC
- Router Solicitation (RS)
- Router Advertisement (RA)
- Automatic IPv6 Address Assignment
- Link-Local Address
- Neighbor Discovery Protocol (NDP)

## Expected Outcome

The PC automatically learns the IPv6 prefix, generates its own IPv6 address, and learns the default gateway from Router Advertisements.
