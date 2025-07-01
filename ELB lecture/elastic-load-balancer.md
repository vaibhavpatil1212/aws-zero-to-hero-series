# 📘 Elastic Load Balancer (ELB) – Key Concepts for Students

## 🔹 1. What is ELB?
Elastic Load Balancer (ELB) is a service provided by AWS that automatically distributes incoming application traffic across multiple targets (like EC2 instances, containers, or IP addresses).

## 🔹 2. Why Use ELB?
- ✅ **High Availability**: Ensures your app is always accessible.
- ✅ **Scalability**: Handles more traffic by distributing it.
- ✅ **Fault Tolerance**: If one server fails, traffic is routed to healthy ones.
- ✅ **Security**: Works with SSL/TLS for secure connections.

## 🔹 3. Types of ELB
| Type | Best For | Description |
|------|----------|-------------|
| **Application Load Balancer (ALB)** | Web apps | Works at Layer 7 (HTTP/HTTPS), supports routing based on URL, headers, etc. |
| **Network Load Balancer (NLB)** | High-performance apps | Works at Layer 4 (TCP/UDP), handles millions of requests per second. |
| **Gateway Load Balancer (GWLB)** | Security appliances | Deploys third-party virtual appliances. |
| **Classic Load Balancer (CLB)** | Legacy apps | Older version, supports basic Layer 4 and 7 routing. |

## 🔹 4. How ELB Works
1. User sends a request (e.g., opens a website).
2. ELB receives the request.
3. ELB checks which backend server is healthy and available.
4. ELB forwards the request to that server.
5. Server responds to the user.

## 🔹 5. Health Checks
ELB regularly checks the health of backend servers. If a server is unhealthy, ELB stops sending traffic to it until it recovers.

## 🔹 6. Real-Life Analogy
Think of ELB like a **traffic police officer** at a busy intersection:
- Directs cars (requests) to open roads (servers).
- Avoids traffic jams (overloaded servers).
- Keeps traffic flowing smoothly.

## 🔹 7. Diagram
![ELB Diagram](elb_diagram.png)
