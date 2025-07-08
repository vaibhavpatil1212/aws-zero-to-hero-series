🌐 What is a CDN?
A Content Delivery Network (CDN) is a system of distributed servers (called edge locations) that deliver web content to users based on their geographic location. The goal is to reduce latency and improve performance.

🚀 What is Amazon CloudFront?
Amazon CloudFront is AWS’s CDN service that:

Caches content at edge locations around the world.
Delivers content over HTTPS with TLS encryption.
Integrates with other AWS services like S3, EC2, Elastic Load Balancing, and Lambda@Edge.
🧩 Key Features
Feature	Description
Global Edge Network	400+ edge locations worldwide for fast content delivery.
Origin Sources	Can pull content from S3, EC2, ALB, or even non-AWS servers.
Caching	Reduces load on origin servers by caching content at edge.
Security	Supports AWS Shield, WAF, signed URLs, and HTTPS.
Lambda@Edge	Run serverless functions at edge locations to customize content.
Real-time Metrics	Integrated with CloudWatch for monitoring and logging.

🧪 How It Works (Simplified Flow)
User Requests Content → e.g., https://d123abc.cloudfront.net/image.jpg
CloudFront Checks Cache at the nearest edge location.
If cached, it serves the content immediately.
If not cached, it fetches from the origin (e.g., S3), caches it, and serves it.
Future requests are served from the cache until TTL expires.
🛠 Use Cases
Static website hosting (via S3 + CloudFront)
Video streaming
API acceleration
Software distribution
Secure content delivery (signed URLs, geo-restriction)

📦 Pricing
CloudFront pricing is based on:

Data transfer out to the internet
Number of HTTP/HTTPS requests
Geographic region
There’s also a Free Tier with 1 TB of data transfer per month for 12 months.
