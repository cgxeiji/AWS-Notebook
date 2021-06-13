# IP Addressing

## IPv4

- It is allocated.
- 4,294,967,296 total IPv4 addr.
- Defined by RFC1918.

### Class A

- From 0.0.0.0 to 127.255.255.255
- Early internet and huge businesses.

- 1 Class A network within 10.x.x.x
    - 16,777,216


### Class B

- From 128.0.0.0 to 191.255.255.255
- Businesses.

- 16 Class B networks from 172.16.x.x to 172.31.x.x
    - 16 x 65,536


### Class C

- From 192.0.0.0 to 223.255.255.255
- Small networks


- 256 Class C networks from 192.168.0.x to 192.168.255.x
    - 256 x 256
    - Home and small networks

### Class D

- Out of the scope of the course.


### Class E

- Out of the scope of the course.



## IPv6

- 340 sextillion
    - 50 cotillion per human alive (8 billion)


## IP Subnettting

Process of braking a larger network into smaller networks.

- /16 is a subset of 10.16.x.x/16 (Class A)
    - Break down to 2 networks:
    - 10.16.0.x/17
        - 10.16.0.x/18
        - 10.16.64.x/18
    - 10.16.128.x/17
        - 10.16.128.x/18
        - 10.16.192.x/18

Each level splits the network range in half!

- 10.16.0.0/16 = 10.16.0.0 ~ 16.16.255.255
    - 10.16.0.0/17 = 10.16.0.0 ~ 10.16.127.255
        - 10.16.0.0/18 = 10.16.0.0 ~ 10.16.63.255
        - 10.16.64.0/18 = 10.16.64.0 ~ 10.16.127.255
    - 10.16.128.0/17 = 10.128.0 ~ 10.16.255.255
        - 10.16.128/18 = 10.16.128.0 ~ 10.16.191.255
        - 10.16.192/18 = 10.16.192.0 ~ 10.16.255.255
