# S3 Replication

- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)


- Replication Configuration can be done from the same account or different
    account.
    - When using a different account, we need to add a Bucket Policy to the
        Destination Bucket to explicitly allow the access from the Role.


## Options

- Replicate all objects or a subset.
- Choose the storage class (default is same as source).
- Ownership (default is the source account).
- Replication Time Control (RTC).
    - Ensure timed sync.


## Considerations

- Not retroactive.
- Versioning must be ON.
- One-way replication from source to destination.
- Can handle unencrypted, SSE-S3, and SSE-KMS (with extra config) objects.
    - NO SSE-C!
- Source bucket owner needs permissions to objects.
- NO system events, Glacier, or Glacier Deep Archive.
- NO DELETES are replicated!!!!


## Why use replication?

- SRR
    - Log Aggregation
    - PROD and TEST sync
    - Resilience with strict data location (sovereignty)
- CRR
    - Global resilience improvements
    - Latency reduction
