# AWS Transfer Family – Technical Documentation

## 1. Overview

AWS Transfer Family provides fully managed support for file transfers directly into and out of Amazon S3 or Amazon EFS using **SFTP, FTPS, and FTP**. It is designed to help you migrate, modernize, or extend legacy file transfer workflows without modifying existing client-side scripts or applications.

---

## 2. Key Features

* ✅ **Protocol Support:** SFTP, FTPS, and FTP
* 🛡️ **Secure Transfers:** Uses IAM, SSH keys, and optionally custom identity providers
* 📂 **Native AWS Integration:** Seamless with Amazon S3 and Amazon EFS
* 🔐 **Audit and Logging:** Integrated with CloudWatch and AWS CloudTrail
* ⚙️ **Scalable and Managed:** No infrastructure to manage

---

## 3. Use Cases

* Legacy systems integration
* Partner file exchange
* Secure transfer to data lakes (S3-based)
* Modern replacement for on-prem FTP servers

---

## 4. Architecture

### Typical Workflow

```
User (via SFTP/FTPS/FTP)
     ↓
AWS Transfer Family (Identity provider validation)
     ↓
Amazon S3 or Amazon EFS (File read/write)
```

---

## 5. Getting Started

### 5.1 Prerequisites

* AWS account
* S3 bucket or EFS file system
* IAM role with proper permissions
* SSH public key (for SFTP users)

### 5.2 Steps to Set Up an SFTP Server

1. **Create an S3 bucket** for file storage.
2. **Open AWS Transfer Family** → Create a server.
3. **Choose protocol(s):** SFTP / FTPS / FTP
4. **Select Identity provider:**

   * Service managed (SSH keys)
   * Custom (Lambda-based)
5. **Add a user:**

   * Specify IAM role
   * Set S3 bucket and home directory
   * Upload SSH public key
6. **Start the server**

---

## 6. Security Configuration

* Use **IAM roles** for controlled access
* Integrate with **AWS Secrets Manager** for credentials
* Enable **CloudWatch logging** for auditing
* Set **IP allowlists** using security groups/VPC endpoints

---

## 7. Monitoring and Logging

* **CloudWatch Logs**: Shows file access activity
* **AWS CloudTrail**: Records API calls
* **CloudWatch Metrics**: Connection counts, upload/download stats

---

## 8. Common Configurations

* Multiple users with isolated folders (chroot-like)
* Custom domain via Route 53 + CloudFront
* Lambda-based identity providers for Active Directory or custom auth

---

## 9. Troubleshooting

* 🔁 **User can't connect?** Check SSH key format or IP restrictions
* 🚫 **Permission denied?** Validate IAM role permissions
* 🔍 **Not seeing logs?** Ensure logging is enabled in server settings

---

## 10. Best Practices

* Prefer **SFTP over FTPS/FTP** for stronger encryption
* Isolate user folders with IAM and logical directories
* Rotate SSH keys and IAM credentials periodically
* Monitor usage and configure CloudWatch alarms

---

## 11. Pricing

* **Hourly rate per endpoint/server**
* **Data transfer per GB**

More details: [AWS Transfer Family Pricing](https://aws.amazon.com/aws-transfer-family/pricing/)

---

## 12. References

* [AWS Transfer Family Documentation](https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html)
* [Amazon S3 Documentation](https://docs.aws.amazon.com/s3/)
* [Amazon EFS Documentation](https://docs.aws.amazon.com/efs/)
