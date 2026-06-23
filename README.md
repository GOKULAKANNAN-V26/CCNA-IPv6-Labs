# Lab 1 - Basic IPv6 Configuration

## Objective

Configure IPv6 addressing on a Cisco router and verify connectivity between a router and a host.

## Topology

PC1 -------- R1

## Configuration

### Router

```bash
ipv6 unicast-routing

interface g0/0
 ipv6 address 2001:DB8:1:1::1/64
 no shutdown
