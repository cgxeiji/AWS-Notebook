# S3 Lifecycle Configuration

- Set of rules.
- Rules are actions.
    - On buckets.
    - On group of objects.
- Transition Actions:
    - Move objects between storage classes.
- Expiration Actions:
    - Remove objects.


## Transitions

Transitions are like a cascade:
- S3 Standard
- S3 Standard-IA
- S3 Intelligent Tiering
- S3 One Zone-IA
- S3 Glacier
- S3 Glacier Deep Archive

Notes:
- There is a minimum of **30 days** on S3 Standard before it can transition.
- Smaller objects can **cost more** (because of minimum size).
- A **single rule** cannot transition from Standard to
    Standard-IA/Intelligent-Tiering/One Zone-IA and immediately to
    Glacier/Glacier Deep Archive. There is a **30 day** cooldown.
