# Lab 2 - EUI-64 Configuration

## Objective

Configure IPv6 EUI-64 on a Cisco router and understand how the Interface ID is automatically generated from the MAC address.

## Topology

PC1 -------- R1

## Configuration

### Router

```bash
ipv6 unicast-routing

interface g0/0
 ipv6 address 2001:DB8:1:1::/64 eui-64
 no shutdown
```

## Verification Commands

```bash
show ipv6 interface brief
show ipv6 interface g0/0
```

## Concepts Learned

- EUI-64
- Interface ID Generation
- MAC Address to IPv6 Conversion
- Link-Local Address
- IPv6 Verification Commands

## Expected Outcome

The router automatically generates the host portion of the IPv6 address using its MAC address.
