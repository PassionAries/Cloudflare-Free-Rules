# Changelog

All notable changes to this project will be documented in this file.

This project follows a simple versioning strategy:

- Major Update (v2027.x)
- Feature Update (v2026.10)
- Patch Update (v2026.07.1)

---

# v2026.07.1 Stable

Release Date: 2026-07

## Initial Stable Release

This is the first production-ready release for Cloudflare Free users.

### Added

#### Rule 1

- ASN Block support

#### Rule 2

- IP List Block support

#### Rule 3

Added vulnerability scanner User-Agent detection.

Supported scanners include:

- sqlmap
- nuclei
- ffuf
- dirsearch
- gobuster
- feroxbuster
- masscan
- zgrab
- TLM-Audit-Scanner

---

#### Rule 4

Added Enterprise Path Block.

Coverage includes:

##### Source Control

- Git
- SVN
- Mercurial

##### Environment

- .env
- .env.local
- .env.production
- .env.development

##### Cloud

- AWS credentials
- Terraform

##### SSH

- authorized_keys
- id_rsa

##### Containers

- Docker
- Docker Compose
- DevContainer

##### Kubernetes

- kubeconfig
- Helm

##### PHP

- phpunit
- phpinfo

##### Laravel

- Ignition
- Storage Logs

##### Spring Boot

- Actuator

##### WordPress

- xmlrpc.php
- wp-login.php
- wp-config.php
- wlwmanifest.xml

##### API

- Swagger
- OpenAPI

##### Logs

- debug.log
- error.log
- laravel.log

##### Database

- dump.sql
- backup.sql

##### Secrets

- config.yml
- config.yaml
- .htpasswd

---

#### Rate Limit

Added Cloudflare Free compatible Rate Limit profile.

Recommended:

- Characteristic: IP
- Requests: 5
- Window: 10 seconds
- Action: Block
- Duration: 10 seconds

---

### Optimized

- Reduced false positives
- Optimized expression length
- Compatible with Cloudflare Free
- Compatible with Managed WAF

---

### Not Blocked

Search engines remain allowed:

- Googlebot
- Bingbot
- Applebot

AI Search remains allowed:

- ChatGPT-User
- Claude-SearchBot
- OAI-SearchBot
- PerplexityBot

---

# Future

## v2026.10

Planned:

- Claude Code
- Gemini CLI
- Cursor 2.x
- Windsurf
- Roo Code
- OpenHands
- New MCP probes

---

## v2027.01

Planned:

- Spring Boot updates
- Next.js
- Laravel updates
- Apache updates
- Nginx updates
- Kubernetes updates
- OCI updates

---

## Maintenance Policy

This project prioritizes:

- Cloudflare Free compatibility
- Low false positives
- Production stability
- Long-term maintainability

Rules may be optimized, reordered, or removed if they no longer provide practical security benefits.
