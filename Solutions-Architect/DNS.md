# Domain Name System (DNS)

- Discovery service.


## DNS Client

- The device that wants to access.


## DNS Resolver

- Software on the device or server which queries DNS.


## Zone

- A part of the DNS database (e.g. google.com)


## Zonefile

- Physical database for a zone.


## Nameserver

- Where zonefiles are hosted.


## Root

- Root Hints: file managed by the OS vendor that configures points at the root servers IPs and addresses.
- Root Server: hosts the DNS root zone.
- Root Zone: points at TLD authoritative servers.
- gTLD: generic top level domain (.com .org).
- ccTLD: country-code top level domain (.uk .eu).


## Time To Live (TTL)

- Time in seconds that a resolver is allowed to cache a zonefile.
- Longer value means faster query but slower update.
- Shorter value means slower query but faster update (of IP, etc).


## DNS Record Types

### A and AAAA Records

- Host to IP
- A: www -> IPv4
- AAAA: www -> IPv6


### CNAME Records

- Canonical Name
- Host to Host (e.g. CNAME ftp -> A server -> IPv4)


### MX Records

- Have priority values (lower means higher priority)
- Find a mail server (SMTP) for a domain
- Requires an A/AAAA record to point to the correct host
- Uses MX Query


### TXT Records

- Input arbitrary text
- Can be queried (Query TXT) to verify ownership of a domain
