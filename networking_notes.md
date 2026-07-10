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
