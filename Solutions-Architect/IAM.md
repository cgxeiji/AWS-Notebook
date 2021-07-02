# IAM Users

- Represents a Single Principal user.
- 5000 IAM Users per account.
- IAM User can be a member of 10 groups.
- There are design impacts.
    - Internet-scale applications
    - Large orgs & org merges
    - IAM Roles & Identity Federation fix this


# IAM Roles

- Suitable for unknown or multiple Principals (users).
- Use for temporary actions.
- They are assumed, you become that role.
- You can attach two policies:
    - Trust Policy: who can access this role
        - Creates temporary security credentials
    - Permissions Policy: AWS permissions


## When to use?

- Lambda Execution Role
    - Applied to AWS Lambda
- Emergency Permissions
- Adding AWS to existing identities
    - Used to allow external accounts to access AWS
    - Called ID Federation
- Cross Account Access
