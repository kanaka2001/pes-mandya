# Chapter 07 — Lab: Amazon S3 (Simple Storage Service)

> ⏰ 12:15 – 12:30 PM | 🧪 Hands-on lab

**By the end of this chapter you can:**
- Explain object storage and core S3 concepts
- Create a bucket and manage objects
- Understand permissions and access policies

---

## 🪣 Core Concepts

| Term | Meaning |
|---|---|
| **Bucket** | A container for objects. Its name is globally unique |
| **Object** | A file plus its metadata, identified by a key |
| **Key** | The unique name of an object in a bucket |
| **Storage class** | Cost and access tier, for example S3 Standard, S3 Glacier |
| **Versioning** | Keeps multiple versions of an object |

> 💡 S3 is designed for 99.999999999% durability ("11 nines") and scales without limit.

---

## 🔐 Access Control

- **Block Public Access** is on by default. Keep it on unless you have a clear need
- **IAM policies** control what identities can do
- **Bucket policies** control access at the bucket level

---

## 🧪 Lab: Create a Bucket and Manage Objects

1. Open **S3** in the Console
2. Choose **Create bucket**
3. Enter a globally unique name, such as `pes-workshop-<yourname>-<number>`
4. Select the Region provided by the facilitator
5. Leave **Block all public access** enabled
6. Choose **Create bucket**
7. Open the bucket and choose **Upload** to add a file
8. Select the object and review its properties
9. Try to open the object URL. You get *Access Denied* because it is private
10. Explore the **Permissions** tab and the bucket policy section
11. (Optional) Enable **Versioning** and upload the file again

---

## 🧹 Clean Up

- Delete the objects, then delete the bucket

---

## ✅ Chapter Checklist

- [ ] Created a bucket with Block Public Access on
- [ ] Uploaded an object
- [ ] Saw that the object is private by default
- [ ] Cleaned up the bucket

---

> ✅ **Next up:**
> ### 👉 [Chapter 08 — Lab: Amazon EC2 & Network/Application Security](08-lab-ec2.md)
