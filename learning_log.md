## Docker Compose

Define multi-container apps in a single YAML file.

```yaml
# docker-compose.yml
version: '3.8'
services:
  web:
    build: .
    ports:
      - '8080:8080'
    depends_on:
      - db
  db:
    image: postgres:15
    environment:
      POSTGRES_PASSWORD: secret
    volumes:
      - pgdata:/var/lib/postgresql/data
volumes:
  pgdata:
```

```bash
docker compose up -d
docker compose logs -f
docker compose down
```


<!-- updated examples -->

## 2026-06-12

Quick session on Docker Images today.

The comparison between approaches was really helpful.

## 2026-06-12

Continued learning about Jules.

Going to revisit this topic next week for deeper understanding.

## Git Rebase

Rebase replays your commits on top of another branch.

```bash
git checkout feature
git rebase main
```

### Merge vs Rebase
| Merge                  | Rebase                  |
|------------------------|-------------------------|
| Creates merge commit   | Linear history          |
| Preserves history      | Rewrites commit hashes  |
| Safe for shared branch | Only for local branches |

**Golden rule:** Never rebase commits that have been pushed to a shared branch.

## DNS Resolution

DNS translates domain names to IP addresses.

### Resolution flow
1. Browser cache → OS cache → Router cache
2. Recursive resolver (ISP)
3. Root nameserver → TLD nameserver → Authoritative nameserver

### Common record types
| Type  | Purpose              | Example            |
|-------|----------------------|--------------------|
| A     | IPv4 address         | 93.184.216.34      |
| AAAA  | IPv6 address         | 2606:2800:220:1::  |
| CNAME | Alias                | www → example.com  |
| MX    | Mail server          | mail.example.com   |
| TXT   | Verification/SPF     | v=spf1 ...         |

```bash
nslookup example.com
dig example.com A
```

## DNS Resolution

DNS translates domain names to IP addresses.

### Resolution flow
1. Browser cache → OS cache → Router cache
2. Recursive resolver (ISP)
3. Root nameserver → TLD nameserver → Authoritative nameserver

### Common record types
| Type  | Purpose              | Example            |
|-------|----------------------|--------------------|
| A     | IPv4 address         | 93.184.216.34      |
| AAAA  | IPv6 address         | 2606:2800:220:1::  |
| CNAME | Alias                | www → example.com  |
| MX    | Mail server          | mail.example.com   |
| TXT   | Verification/SPF     | v=spf1 ...         |

```bash
nslookup example.com
dig example.com A
```

## 2026-07-12

Today I focused on Claude Code.

Connecting this to what I learned last week about related concepts.


<!-- updated examples -->
