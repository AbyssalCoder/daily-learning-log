## GitHub Actions — CI/CD

```yaml
# .github/workflows/ci.yml
name: CI
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: '3.11'
      - run: pip install -r requirements.txt
      - run: python -m pytest
```

Workflows live in `.github/workflows/` and trigger on events.

## Nginx Basics

Nginx is a high-performance web server and reverse proxy.

### Basic config
```nginx
server {
    listen 80;
    server_name example.com;

    location / {
        root /var/www/html;
        index index.html;
    }

    location /api {
        proxy_pass http://localhost:3000;
    }
}
```

```bash
sudo nginx -t           # Test config
sudo systemctl reload nginx  # Reload
```
