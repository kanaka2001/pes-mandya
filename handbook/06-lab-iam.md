# AWS Identity and Access Management (IAM)

**Time:** 12:00 – 12:15 PM | **Hands-on lab**

## Learning objectives

- Distinguish authentication and authorization.
- Create users, groups, and roles.
- Apply the Principle of Least Privilege.

## 6.1 Concepts

| Term | Meaning |
|---|---|
| **Authentication** | Proving who you are. |
| **Authorization** | Deciding what you are allowed to do. |
| **User** | An identity for a person or application. |
| **Group** | A collection of users sharing permissions. |
| **Role** | An identity with permissions that can be assumed temporarily. |
| **Policy** | A JSON document defining permissions. |

## 6.2 Role-Based Access Control (RBAC)

Permissions are given to roles or groups based on job function, and users receive access by belonging to them. This keeps access consistent and easy to manage.

## 6.3 Principle of Least Privilege

Grant only the permissions needed for a task, and nothing more.

Example policy (read-only access to one bucket):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:ListBucket"],
      "Resource": [
        "arn:aws:s3:::my-workshop-bucket",
        "arn:aws:s3:::my-workshop-bucket/*"
      ]
    }
  ]
}
```

## 6.4 Lab: IAM setup

1. Open **IAM** in the AWS Console.
2. Go to **User groups** and choose **Create group**. Name it `workshop-readonly`.
3. Attach a managed policy such as `AmazonS3ReadOnlyAccess`.
4. Go to **Users** and choose **Create user**. Name it `workshop-user`.
5. Add the user to the `workshop-readonly` group.
6. Review the user's permissions tab.
7. (Optional) Enable MFA.
8. Review how a **role** differs from a user.

## Best practices

- Do not use the root account for daily work.
- Enable MFA.
- Use roles instead of long-term access keys.
- Review permissions regularly.

## Key takeaways

- Authentication is who you are. Authorization is what you can do.
- Start with minimal permissions and add only as needed.

---

[← Previous: Transition, Q&A & Lab Readiness Check](05-readiness-check.md) | [Home](README.md) | [Next: Amazon S3 (Simple Storage Service) →](07-lab-s3.md)
