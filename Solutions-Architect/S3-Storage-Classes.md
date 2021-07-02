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
