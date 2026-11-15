# Chapter 06 — Lab: AWS Identity and Access Management (IAM)

> ⏰ 12:00 – 12:15 PM | 🧪 Hands-on lab

**By the end of this chapter you can:**
- Distinguish authentication and authorization
- Create users, groups, and roles
- Apply the Principle of Least Privilege

---

## 🔑 Concepts

| Term | Meaning |
|---|---|
| **Authentication** | Proving who you are |
| **Authorization** | Deciding what you are allowed to do |
| **User** | An identity for a person or application |
| **Group** | A collection of users sharing permissions |
| **Role** | An identity with permissions that can be assumed temporarily |
| **Policy** | A JSON document defining permissions |

---

## 👥 Role-Based Access Control (RBAC)

Permissions are given to roles or groups based on job function. Users receive access by belonging to them. This keeps access consistent and easy to manage.

---

## 🔒 Principle of Least Privilege

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

---

## 🧪 Lab: IAM Setup

1. Open **IAM** in the AWS Console
2. Go to **User groups** and choose **Create group**. Name it `workshop-readonly`
3. Attach a managed policy such as `AmazonS3ReadOnlyAccess`
4. Go to **Users** and choose **Create user**. Name it `workshop-user`
5. Add the user to the `workshop-readonly` group
6. Review the user's **Permissions** tab
7. (Optional) Enable MFA
8. Review how a **role** differs from a user

---

## 🌟 Best Practices

- Do not use the root account for daily work
- Enable MFA
- Use roles instead of long-term access keys
- Review permissions regularly

---

## ✅ Chapter Checklist

- [ ] Created the `workshop-readonly` group
- [ ] Created `workshop-user` and added it to the group
- [ ] I can explain least privilege in one sentence

---

> ✅ **Next up:**
> ### 👉 [Chapter 07 — Lab: Amazon S3](07-lab-s3.md)
