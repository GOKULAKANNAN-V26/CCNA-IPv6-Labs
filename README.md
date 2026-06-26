# Lab 4 - Stateless DHCPv6

## Objective

Configure Stateless DHCPv6 and understand how a host receives DNS information from DHCPv6 while generating its own IPv6 address using SLAAC.

## Topology

PC1 -------- R1

## Configuration

### DHCPv6 Pool

```bash
ipv6 dhcp pool DNS_POOL
 dns-server 2001:DB8::53
 domain-name ccna.local
```

### Interface Configuration

```bash
interface g0/0
 ipv6 address 2001:DB8:1:1::1/64
 ipv6 nd other-config-flag
 ipv6 dhcp server DNS_POOL
 no shutdown
```

### PC

Desktop → IP Configuration

Select:

IPv6 Auto Config

## Verification Commands

```bash
show ipv6 dhcp pool
show ipv6 interface g0/0
show ipv6 neighbors
```

## Concepts Learned

- Stateless DHCPv6
- O Flag (Other Configuration Flag)
- DNS Distribution through DHCPv6
- SLAAC
- Router Advertisement (RA)

## Expected Outcome

The host creates its own IPv6 address using SLAAC and receives DNS information from the DHCPv6 server.
