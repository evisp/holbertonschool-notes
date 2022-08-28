# Load balancer

## What is a load balancer?

- A **load balancer** acts as the *traffic cop* sitting in front of your servers and routing client requests across all servers capable of fulfilling those requests in a manner that maximizes speed and capacity utilization and ensures that no one server is overworked, which could degrade performance. 
  - If a single server goes down, the load balancer redirects traffic to the remaining online servers. When a new server is added to the server group, the load balancer automatically starts to send requests to it.
[Load-balancer](https://holbertonintranet.s3.amazonaws.com/uploads/medias/2020/9/6cefdd14b2f8c36789cba132bd5a10d42d88a177.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOU5BHMTQX4%2F20220828%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220828T174633Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=38b41f9ec6ac495cbca82db437b5a3c754d4d3c538405a9d3714e377464f5f58)

### Load balancer functions
- Distributes client requests or network load efficiently across multiple servers
- Ensures high availability and reliability by sending requests only to servers that are online
- Provides the flexibility to add or subtract servers as demand dictates

### Load balancer algorithm
- **Round Robin** - requests are distributed across the group of servers sequentially
- **Least Connections** - a new request is sent to the server with the fewest current connections to clients. The relative computing capacity of each server is factored into determining which one has the least connections
- **Least Time** – Sends requests to the server selected by a formula that combines the fastest response time and fewest active connections. Exclusive to NGINX Plus.
- **Hash** – Distributes requests based on a key you define, such as the client IP address or the request URL. NGINX Plus can optionally apply a consistent hash to minimize redistribution
of loads if the set of upstream servers changes.
- **IP Hash** – The IP address of the client is used to determine which server receives the request
