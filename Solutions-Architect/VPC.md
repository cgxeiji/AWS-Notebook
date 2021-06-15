# Virtual Private Cloud (VPC)

## Basics

- Virtual network inside AWS.
- Lives within 1 account & 1 region.
- Private and isolated by default.
- Two types:
    - Default: only 1 per region.
    - Custom: many per region.


### VPC CIDR

- Classless Inter-Domain Routing (CIDR).
- Default VPC always has the same address: 172.31.0.0/16.
    - Includes a /20 subnet in each AZ in the region.
