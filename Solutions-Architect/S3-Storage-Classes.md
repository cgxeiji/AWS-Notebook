# S3 Storage Classes

## S3 Standard

- When objects are stored, expect a HTTP/1.1 200 OK response.
- For 10,000,000 objects, 1 object loss per 10,000 years (99.9999~%
    durability).
- Replication over 3AZs + Content-MD5 Checksums.
- Cyclic Redundancy Checks (CRCs) are used to detect data corruption.


- Use this for **frequently accessed data** which is important and
    non-replaceable.


## S3 Standard-IA (Infrequent Access)

- Similar to S3 Standard.
- Lower cost.
- Has a retrieval fee (which increases with frequent access) + transfer fee.
- Minimum duration charge of 30 days.
- Minimum of 128KB per object.


- Use this for **long-lived data** which is important but is accessed infrequently.


## S3 One Zone-IA

- Similar to Standard-IA.
- Only uses one zone (less reliability).


- Use this for **long-lived data** which is not important, replaceable, and
    accessed infrequently.


## S3 Glacier

- Similar to Standard.
- 1/5 of the cost.
- Object **cannot be made public**.
    - Requires a retrieval process.
- Glacier is retrieved to Standard-IA temporarily:
    - Expedited (1-5 min)
    - Standard (3-5 h)
    - Bulk (5-12 h)
    - Faster = More expensive!


- Use this for **archival data** where frequent or real-time access isn't
    needed.


## S3 Glacier Deep Archive

- Similar to Glacier.
- 1/4 of the cost.
- Glacier is retrieved to Standard-IA temporarily:
    - Standard (12 h)
    - Bulk (up to 48 h)
    - Faster = More expensive!


- Use this for **archival data** that rarely needs to be accessed (e.g. Legal
    or Regulation data storage).


## S3 Intelligent-Tiering

- Monitors and automatically moves objects between storage classes.
- Objects not accessed for 30 days are moved to infrequent access.
- There are no retrieval fees.
- Cost per 1,000 objects for monitoring and automation.
- Cost per storage type (similar to direct storage classes).


- Use this for **long-lived data** with changing or unknown patterns.
