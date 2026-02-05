# Scaling and Load Balancing in a Live Project


## Why Scaling Is Required

Scaling is the ability of a system to **handle increased load (users, requests, and data)** without compromising performance. As traffic grows, servers can become overloaded, leading to slow responses, failures, and poor user experience. Proper scaling ensures:

- High availability  
- Better reliability  
- Improved performance  
- Enhanced user experience  

---

## Role of Load Balancers

A **load balancer** sits between clients and backend servers and distributes incoming requests across multiple servers. Instead of all requests hitting a single server, the load balancer intelligently routes traffic to healthy servers using algorithms such as:

- **Round Robin**
- **Least Connections**
- **IP Hash**

Load balancers also perform **health checks**, automatically removing unhealthy servers from traffic rotation. This improves **fault tolerance**—even if one server crashes, the system continues to function without impacting users.

**Common Load Balancers:**
- NGINX  
- HAProxy  
- AWS Elastic Load Balancer (ELB)  

---

## Vertical Scaling (Scale Up)

Vertical scaling means **increasing the capacity of an existing server** by adding more CPU, RAM, or storage.

### Advantages
- Simple to implement  
- No code changes required  
- Suitable for monolithic applications  

### Limitations
- Hardware limits exist  
- Downtime may be required  
- Single point of failure remains  
- Expensive at higher levels  

Vertical scaling works well in the **initial stages**, but it is not a long-term solution for high-traffic systems.

---

## Horizontal Scaling (Scale Out)

Horizontal scaling involves **adding more servers** and distributing the load across them using a load balancer.

### Advantages
- High availability  
- Fault tolerance  
- Virtually unlimited scaling  
- Cost-effective using cloud infrastructure  

### Challenges
- Requires stateless application design  
- Session management using Redis or similar tools  
- More complex system architecture  

Modern applications prefer **horizontal scaling**, especially in **microservices** and **cloud-native systems**.

---

## Sources


1. [Load Balancing Basics - NGINX Docs](https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/)  
2. [System Design Basics - GeeksforGeeks](https://www.geeksforgeeks.org/scaling-in-system-design/)  
