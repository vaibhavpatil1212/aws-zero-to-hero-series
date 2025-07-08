# AWS CDN with Amazon CloudFront

This guide provides an overview of AWS's Content Delivery Network (CDN) service using **Amazon CloudFront**, along with a practical lab to help you set up your own CDN.

## 📦 What is a CDN?

A **Content Delivery Network (CDN)** is a globally distributed network of servers that delivers content to users based on their geographic location, improving speed and performance.

### ✅ Benefits of Using AWS CloudFront
- Low latency and high transfer speeds
- Integrated with AWS services like S3, EC2, and Lambda@Edge
- Secure content delivery with HTTPS and signed URLs
- Real-time metrics and logging via CloudWatch

---

## 🧪 Lab: Create a CDN Using AWS CloudFront

### Prerequisites
- AWS account (Free Tier is sufficient)
- Basic knowledge of AWS S3 and IAM

---

### Step 1: Upload Content to S3
1. Go to the **S3 Console**.
2. Create a new bucket (e.g., `my-cdn-content`).
3. Upload static files (e.g., images, HTML, CSS).
4. Make the files public or configure bucket policy for CloudFront access.

---

### Step 2: Create a CloudFront Distribution
1. Open the **CloudFront Console**.
2. Click **Create Distribution**.
3. Under **Origin Settings**:
   - Origin domain: Select your S3 bucket.
   - Viewer protocol policy: Redirect HTTP to HTTPS.
4. Under **Default Cache Behavior**:
   - Allowed HTTP methods: GET, HEAD
   - Cache policy: Use default or create a custom one.
5. Click **Create Distribution**.

> ⚠️ It may take 10–20 minutes for the distribution to deploy.

---

### Step 3: Access Your CDN
- Once deployed, use the **CloudFront domain name** (e.g., `d123abc.cloudfront.net`) to access your content.
- Example: `https://d123abc.cloudfront.net/image.jpg`

---

### Step 4: Optional Enhancements
- 🔐 Enable **Signed URLs** or **Geo-restrictions** for secure delivery.
- 🧠 Use **Lambda@Edge** for real-time content manipulation.
- 📊 Monitor performance with **CloudWatch** metrics and logs.

---

## 📚 Resources
- Amazon CloudFront Documentation
- AWS Free Tier
- Lambda@Edge

---

## 🛠 Author
Created by [Your Name]  
Feel free to fork and contribute!

