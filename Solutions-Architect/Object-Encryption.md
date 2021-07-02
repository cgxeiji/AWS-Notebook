# Object Encryption

- Client-Side
    - No clue of the data
    - Client controls key and encryption.
- Server-Side
    - Data comes raw and you can decide the encryption.


- Server-Side Encryption with Customer-Provided Keys (SSE-C)
    - Used when client needs to manage keys, but the encryption process can be server side.
- Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
    - AES256.
    - Users provide plaintext data.
    - Keys are outside of your control.
    - For most cases, default encryption method.
    - Not suitable for role separation.
- Server-Side Encryption with Customer Master Keys (CMKs) Stored in AWS Key
    Management Service (SSE-KMS)
    - Users provide plaintext data.
    - Keys are outside of your control.
    - KMS manages the CMK.
    - Suitable for role separation.
