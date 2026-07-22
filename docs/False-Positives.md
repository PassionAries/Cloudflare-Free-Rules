# False Positives

This document records known false positives and design decisions.

---

## General Principles

The project prioritizes:

- Production stability
- Low false positives
- Cloudflare Free compatibility

---

## Intentionally NOT Blocked

### Search Engines

- Googlebot
- Bingbot
- Applebot

Reason:

Blocking them may affect search engine indexing.

---

### AI Search

- ChatGPT-User
- OAI-SearchBot
- Claude-SearchBot
- PerplexityBot
- Perplexity-User

Reason:

These crawlers are used for AI search and user-requested retrieval.

---

## Generic HTTP Libraries

Not blocked.

Examples:

- curl
- wget
- python-requests
- Go-http-client
- okhttp

Reason:

Widely used by legitimate software.

---

## Path Rules

Avoid matching:

- continue
- config.json
- api
- login
- admin

Reason:

High false positive rate.

---

## Maintenance

If a path causes repeated false positives:

1. Verify logs.
2. Confirm the application behavior.
3. Update the rule in the next release.

---

Last Updated

v2026.07.1 Stable
