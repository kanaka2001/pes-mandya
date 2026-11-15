# Amazon S3 (Simple Storage Service)

**Time:** 12:15 – 12:30 PM | **Hands-on lab**

## Learning objectives

- Explain object storage and core S3 concepts.
- Create a bucket and manage objects.
- Understand permissions and access policies.

## 7.1 Core concepts

| Term | Meaning |
|---|---|
| **Bucket** | A container for objects. Its name is globally unique. |
| **Object** | A file plus its metadata, identified by a key. |
| **Key** | The unique name of an object in a bucket. |
| **Storage class** | Cost and access tier, for example S3 Standard, S3 Glacier. |
| **Versioning** | Keeps multiple versions of an object. |

S3 offers high durability (designed for 99.999999999%, "11 nines") and scales without limit.

## 7.2 Access control

- **Block Public Access** is on by default. Keep it on unless you have a clear need.
- **IAM policies** control what identities can do.
- **Bucket policies** control access at the bucket level.

## 7.3 Lab: create a bucket and manage objects

1. Open **S3** in the Console.
2. Choose **Create bucket**.
3. Enter a globally unique name, such as `pes-workshop-<yourname>-<number>`.
4. Select the Region provided by the facilitator.
5. Leave **Block all public access** enabled.
6. Choose **Create bucket**.
7. Open the bucket and choose **Upload** to add a file.
8. Select the object and review its properties.
9. Try to open the object URL and note the result (access denied, because it is private).
10. Explore the **Permissions** tab and view the bucket policy section.
11. (Optional) Enable **Versioning** and upload the file again.

## Clean up

- Delete the objects, then delete the bucket.

## Key takeaways

- S3 stores objects in buckets, and is private by default.
- Access is controlled through policies.

---

[← Previous: AWS Identity and Access Management (IAM)](06-lab-iam.md) | [Home](README.md) | [Next: Amazon EC2 & Network/Application Security →](08-lab-ec2.md)
