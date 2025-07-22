# Static-Website-Hosting 🚀

This repository automates the deployment of a simple static website to AWS S3 with static‑website hosting enabled.

---

## 📦 Structure

- **/website/** – Contains all website assets (`index.html`, `404.html`, CSS, images, JS).
- **/infra/** – Holds AWS bucket policy and any deployment scripts.

---

## ✅ Features

- Enables S3 static website hosting.
- Configures a public bucket policy for read access.
- Hosts `index.html` and `404.html` properly.
- (Optional) Upload automation via `deploy.sh`.

---

## ⚙️ Usage

1. Create S3 bucket and enable static hosting.
2. Apply the AWS bucket policy:
   ```bash
   aws s3api put-bucket-policy \
     --bucket YOUR_BUCKET_NAME \
     --policy file://infra/bucket-policy.json
