# Network Address Translation (NAT)

- NAT improves over IPv4. (IPv6 does not need any translation service)
- Is more secure.


## Static NAT

- 1 private to 1 fixed public (IGW).
- NAT Table maps 1 private : 1 public addresses.


## Dynamic NAT

- 1 private to 1st available public.
- Temporary allocates from a public IP Pool.


## Port Address Translation (PAT)

- Many private to 1 public (NATGW).
- AWS NATGateway uses this.
- As long as the src port is unique, many private IP can use the same public
    IP.
