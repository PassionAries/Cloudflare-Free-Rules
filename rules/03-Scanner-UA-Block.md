# Rule 03 - Scanner User-Agent Block

## Purpose

Block requests from known vulnerability scanners while allowing legitimate search engines and AI search crawlers.

This rule targets offensive security tools that identify themselves through the HTTP User-Agent header.

It intentionally **does not block** major search engines or AI search indexing services.

---

## Action

Block

---

## Cloudflare Expression

See:

expressions/03-Scanner-UA.cf

---

## Rule Name

Scanner User-Agent Block

---

## Recommended Priority

3

This rule should be evaluated after ASN Block and IP Block.

---

## Supported Scanners

Current signatures include:

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

## Allowed Crawlers

The following crawlers are intentionally NOT blocked.

### Search Engines

- Googlebot
- Bingbot
- Applebot

### AI Search

- ChatGPT-User
- OAI-SearchBot
- Claude-SearchBot
- PerplexityBot
- Perplexity-User

Blocking these may reduce search visibility or AI indexing.

---

## Why Block by User-Agent?

Although User-Agent can be spoofed, many automated scanners still use their default identifiers.

Blocking them reduces:

- Background Internet scanning
- Automated vulnerability probing
- Noise in logs
- Low-effort reconnaissance

---

## False Positives

Very Low

Only well-known offensive security tools are matched.

Common browsers and search engines are unaffected.

---

## Maintenance

Add new scanner signatures only after they are observed in the wild.

Avoid generic keywords that may affect legitimate software.

---

## Change History

### v2026.07.1

Initial stable release.
