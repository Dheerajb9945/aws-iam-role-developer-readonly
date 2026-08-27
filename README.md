# aws-iam-role-developer-readonly
# AWS IAM Role - Developer Read-Only Access

## Project Overview

Created an AWS IAM Role setup that gives a developer temporary read-only access to AWS resources.

## Company Scenario

Developers need to view AWS resources but should not be able to modify or delete them.

## Objective

Create an IAM User, IAM Role, and allow the user to assume the role with read-only permissions.

## Architecture
Developer-User
      ↓
sts:AssumeRole
      ↓
Developer-ReadOnly-Role
      ↓
ReadOnlyAccess
      ↓
Read 
## AWS Services Used

* AWS IAM
* AWS STS

## IAM User Created

`Developer-User`

## IAM Role Created

`Developer-ReadOnly-Role`

## Role Permissions

`ReadOnlyAccess`

## Trust Relationship

Allows the AWS account to assume the role.

## AssumeRole Policy

Allows `Developer-User` to use:

```text
sts:AssumeRole
```

## Implementation Steps

1. Created `Developer-User`.
2. Created `Developer-ReadOnly-Role`.
3. Attached `ReadOnlyAccess`.
4. Configured the trust relationship.
5. Allowed the user to assume the role.
6. Switched to the role and tested access.

## Testing

### Read Access

**Result:** Successful ✅

## What I Learned

* IAM Users vs IAM Roles
* Trust relationships
* `sts:AssumeRole`
* Temporary role access
* Least privilege

## Security Considerations

* Avoid unnecessary AdministratorAccess.
* Use least-privilege permissions.
* 
## Screenshots

1. IAM User Created
2. IAM Role Created
3. ReadOnlyAccess
4. Trust Relationship
5. AssumeRole Policy
6. Successful Role Switch
7. Read Access
