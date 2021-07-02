# Key Management Service (KMS)

- Regional and Public service.
- Create, store and manage keys.
- Symmetric and asymmetric keys.
- Cryptographic operations.
- Keys never leave KMS (compliant with FIPS 140-2 (L2)).


## Customer Master Keys (CMK)

- Is logical: ID, date, policy, desc, state.
- Backed by jhysical key material.
- Generated or imported.
- CMK can be used for up to 4KB of data!


## Data Encryption Keys (DEK)

- GenerateDataKey: works on more than 4KB data.
- Plaintext Version
- Ciphertext Version
    - Encrypt data using plaintext key
    - Discard key
    - Store encrypted key with data


## Exam!

- CMKs are isolated to a region and never leave.
- AWS Managed or Customer Managed CMKs.
- Customer managed keys are more configurable.
- CMKs support rotation.
    - AWS Manged key is on (every 3 years rotation).
    - Customer Managed is off by default (every 1 year rotation).
- Backing key and previous backing keys.
- Have per region aliases.


## Key Policies and Security

- Every CMK has one policy.
- Usually Key Policies + IAM Policies together.


Notes:

- CreateKey, Encrypt, and Decrypt have different permissions. (Role separation)
