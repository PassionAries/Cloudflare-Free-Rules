# Rule 04 - Enterprise Path Block

## Purpose

Block requests attempting to enumerate sensitive files, credentials, source code, cloud configuration, AI development environments, CI/CD pipelines, and common vulnerability disclosure endpoints.

This rule is the primary protection against automated reconnaissance.

---

## Action

Block

---

## Expression

See:

expressions/04-Enterprise-Path.cf

---

## Categories

The expression is organized into the following groups:

1. Environment Files
2. Source Control
3. Cloud Credentials
4. SSH
5. Containers
6. Kubernetes
7. Terraform
8. CI/CD
9. AI IDE
10. PHP
11. WordPress
12. Laravel
13. Spring Boot
14. Database
15. Logs
16. Secrets
17. API Documentation

---

## Design Goals

- Compatible with Cloudflare Free
- Low false positives
- Easy maintenance
- Optimized expression length

---

## Rule Priority

4

---

## Maintenance

New paths should only be added after observing real-world scanning activity.

Avoid matching generic application paths that may cause false positives.

---

## False Positives

Low

---

## Change History

### v2026.07.1

Initial release.
