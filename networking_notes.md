## Caching Strategies

### Where to cache
- Browser cache (Cache-Control headers)
- CDN (edge caching)
- Application cache (Redis, Memcached)
- Database query cache

### Cache invalidation strategies
- **TTL** — expire after time
- **Write-through** — update cache on write
- **Write-behind** — async cache update
- **Cache-aside** — app manages cache explicitly

> "There are only two hard things in CS: cache invalidation and naming things."

## Load Balancers

Distribute incoming traffic across multiple servers.

### Algorithms
- **Round Robin** — rotate through servers
- **Least Connections** — send to least busy
- **IP Hash** — consistent routing by client IP
- **Weighted** — proportional to server capacity

### Layer 4 vs Layer 7
- L4: routes based on IP/port (faster)
- L7: routes based on HTTP content (smarter)

Tools: Nginx, HAProxy, AWS ALB/NLB

## Network Monitoring Commands

```bash
# Check connectivity
ping google.com

# Trace route to host
traceroute google.com   # Linux
tracert google.com      # Windows

# View active connections
netstat -tuln
ss -tuln                # modern alternative

# DNS lookup
nslookup example.com
dig example.com

# Capture packets
tcpdump -i eth0 port 80
```


<!-- formatting -->


