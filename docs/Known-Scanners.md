# Known Scanners

This document tracks vulnerability scanners, reconnaissance tools, and offensive security frameworks observed in the wild.

Only scanners with practical value should be added to the User-Agent rule.

---

# Supported (Blocked)

## SQL Injection

| Tool | Status |
|------|--------|
| sqlmap | ✅ |

---

## Web Vulnerability Scanners

| Tool | Status |
|------|--------|
| nuclei | ✅ |
| TLM-Audit-Scanner | ✅ |
| OpenVAS | Planned |
| Nessus | Planned |
| Acunetix | Planned |
| Netsparker | Planned |

---

## Directory Enumeration

| Tool | Status |
|------|--------|
| ffuf | ✅ |
| gobuster | ✅ |
| dirsearch | ✅ |
| feroxbuster | ✅ |
| wfuzz | Planned |

---

## Network Scanners

| Tool | Status |
|------|--------|
| masscan | ✅ |
| zgrab | ✅ |
| zmap | Planned |
| naabu | Planned |
| rustscan | Planned |

---

## HTTP Libraries

These are intentionally NOT blocked because they are commonly used by legitimate applications.

- curl
- wget
- python-requests
- Go-http-client
- okhttp
- Java

Blocking these would create unnecessary false positives.

---

## Search Engines

Allowed.

- Googlebot
- Bingbot
- Applebot

---

## AI Search

Allowed.

- ChatGPT-User
- OAI-SearchBot
- Claude-SearchBot
- PerplexityBot
- Perplexity-User

---

## Maintenance Policy

Only add scanners that:

- Clearly identify themselves
- Are widely used
- Produce significant attack traffic

Avoid adding generic libraries or browsers.

---

## Last Updated

v2026.07.1 Stable
