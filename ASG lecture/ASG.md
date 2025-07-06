📘 AWS Auto Scaling Group (ASG) - Theory Guide

---

## 🔹 What is Auto Scaling Group (ASG)?

An **Auto Scaling Group (ASG)** in AWS automatically adjusts the number of EC2 instances based on demand. It ensures that the desired number of healthy instances is always running.

---

## ✅ Key Benefits of Auto Scaling

- ✅ **High Availability**: Maintains desired instance count, replaces failed instances
- ⚖️ **Elasticity**: Scales resources in/out as demand changes
- 💸 **Cost Optimization**: Avoids over-provisioning by removing idle capacity
- 🔁 **Fault Tolerance**: Automatically replaces unhealthy instances

---

## 🔧 Main Components of ASG

| Component           | Description |
|--------------------|-------------|
| **Launch Template**| EC2 instance config: AMI, type, key pair, user data, etc. |
| **Auto Scaling Group** | Manages and maintains EC2 instance group |
| **Scaling Policies**| Rules to scale in/out based on metrics |
| **Health Checks**   | EC2 or ELB-based checks to detect and replace unhealthy instances |
| **Desired Capacity**| Number of instances to maintain |
| **Min/Max Capacity**| Lower and upper limits for instances |
| **Subnets & AZs**   | Multi-AZ distribution for high availability |

---

## ⚙️ Types of Scaling Policies

1. **Target Tracking Scaling**
   - Automatically adjusts based on a defined metric (e.g., average CPU = 50%)

2. **Step Scaling**
   - Scales in defined steps based on thresholds (e.g., add 1 instance if CPU > 70%)

3. **Scheduled Scaling**
   - Scales resources based on time-based schedule

---

## 📊 Common Use Cases

- Scalable web apps with unpredictable traffic
- Backend services needing high uptime
- Batch jobs and worker queues
- Reducing cost during off-peak hours

---

## 🛑 When ASG Terminates an Instance

- Fails a health check
- Scaling in based on low resource usage
- Scheduled scale-in time triggers

---

## 📝 Best Practices

- Use **ALB/NLB** for traffic distribution
- Configure **CloudWatch Alarms** to monitor metrics
- Set appropriate **IAM roles** and **security groups**
- Use **multi-AZ deployment** for higher fault tolerance

---
