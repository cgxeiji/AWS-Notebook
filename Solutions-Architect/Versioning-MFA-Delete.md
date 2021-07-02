# Object Versioning

- Cannot be switched off, only suspended.
- Space is consumed by ALL versions.
- You are billed for ALL versions.
- You can only nuke the bucket.

- Bucket
    - Disabled -> Enabled (NOT REVERSIBLE)
    - Enabled -> Suspended (REVERSIBLE)


# MFA Delete

- MFA is required to change bucket versioning state.
- MFA is required to delete versions.
- Serial number (MFA) + code passed with API calls.
