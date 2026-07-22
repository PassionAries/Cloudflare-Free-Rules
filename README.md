# Cloudflare Free Rules

> Cloudflare Free WAF Rules for Production
>
> Version: **v2026.07.1 Stable**

---

## Project Goal

This project maintains a production-ready Cloudflare Free WAF ruleset focused on:

- Blocking vulnerability scanners
- Blocking sensitive file enumeration
- Blocking source code leaks
- Blocking cloud credential discovery
- Blocking AI IDE / MCP / DevContainer scanning
- Keeping false positives as low as possible
- Fully compatible with **Cloudflare Free Plan**

This project **does not require Cloudflare Pro or Enterprise**.

---

# Features

✅ Cloudflare Free compatible

✅ Low false positives

✅ Production ready

✅ Versioned releases

✅ Long-term maintenance

---

# Rule Layout

| Rule | Description | Action |
|------|-------------|--------|
| Rule 1 | ASN Block | Block |
| Rule 2 | IP Block | Block |
| Rule 3 | Scanner User-Agent | Block |
| Rule 4 | Enterprise Path Block | Block |
| Rule 5 | Reserved | Reserved |

---

# Rate Limit

Recommended configuration:

Expression:

See:

```
rules/05-Rate-Limit.md
```

Settings:

- Characteristic: IP
- Requests: 5
- Period: 10 seconds
- Action: Block
- Duration: 10 seconds

---

# Supported Protection

## Sensitive Files

- .env
- .git
- .svn
- .hg
- .aws
- .ssh

## Cloud

- AWS
- Terraform

## Containers

- Docker
- Docker Compose
- DevContainer

## Kubernetes

- kubeconfig
- Helm

## AI IDE

- Cursor
- Claude Code
- Codeium
- MCP
- Roo Code
- OpenHands

## PHP

- phpunit
- phpinfo

## WordPress

- xmlrpc.php
- wp-login.php
- wp-config.php
- wlwmanifest.xml

## Laravel

- Ignition
- Storage Logs

## Spring Boot

- Actuator

## API

- Swagger
- OpenAPI

---

# Search Engines

This project intentionally **does NOT block**:

- Googlebot
- Bingbot
- Applebot
- ChatGPT-User
- OAI-SearchBot
- Claude-SearchBot
- PerplexityBot

Only vulnerability scanners are blocked.

---

# Repository Structure

```
Cloudflare-Free-Rules/

README.md
CHANGELOG.md
LICENSE

rules/
    01-ASN-Block.md
    02-IP-Block.md
    03-Scanner-UA-Block.md
    04-Enterprise-Path-Block.md
    05-Rate-Limit.md

docs/
    Known-Scanners.md
    Known-Paths.md
    False-Positives.md
    Roadmap.md
```

---

# Versioning

Current Version

```
v2026.07.1 Stable
```

Future Releases

```
v2026.10
v2027.01
v2027.04
```

---

# Cloudflare Compatibility

| Plan | Supported |
|------|-----------|
| Free | ✅ |
| Pro | ✅ |
| Business | ✅ |
| Enterprise | ✅ |

Optimized for **Cloudflare Free Plan**.

---

# Contributing

Future releases will include:

- New vulnerability scanners
- New AI IDE probes
- New MCP paths
- New cloud credential paths
- False positive optimizations

---

# License

MIT License
