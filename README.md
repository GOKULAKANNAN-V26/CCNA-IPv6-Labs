# Lab 5 - Stateful DHCPv6

## Objective

Configure Stateful DHCPv6 and understand how a DHCPv6 server assigns IPv6 addresses, DNS information, and domain information to clients.

## Topology

PC1 -------- R1

## Configuration

### DHCPv6 Pool

```bash
ipv6 dhcp pool STATE_POOL
 address prefix 2001:DB8:1:1::/64
 dns-server 2001:DB8::53
 domain-name ccna.local
```

### Interface Configuration

```bash
interface g0/0
 ipv6 address 2001:DB8:1:1::1/64
 ipv6 nd managed-config-flag
 ipv6 dhcp server STATE_POOL
 no shutdown
```

### PC

Desktop → IP Configuration

Select:

IPv6 Auto Config

## Verification Commands

```bash
show ipv6 dhcp pool
show ipv6 dhcp binding
show ipv6 interface g0/0
```

## Concepts Learned

- Stateful DHCPv6
- M Flag (Managed Configuration Flag)
- DHCPv6 Address Assignment
- DHCPv6 Bindings
- Router Advertisement (RA)

## Expected Outcome

The DHCPv6 server assigns IPv6 addresses, DNS information, and domain information to the host.
