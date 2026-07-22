# Rule 02 - IP Block

## Purpose

Block requests from IP addresses that have been confirmed as malicious.

Unlike ASN blocking, this rule targets individual IP addresses that repeatedly perform:

- Vulnerability scanning
- Credential stuffing
- Exploit attempts
- Malicious automation
- Persistent abuse

This rule is intended to be updated regularly.

---

## Action

```
Block
```

---

## Cloudflare Expression

```cf
ip.src in $bad_scanners
```

---

## Rule Name

```
IP Block
```

---

## Recommended Priority

```
2
```

This rule should be evaluated immediately after the ASN Block rule.

---

## Why Use an IP List?

Using a Cloudflare List has several advantages:

- No need to edit the WAF rule
- Faster updates
- Easier maintenance
- Supports bulk imports
- Keeps expressions short

Only the contents of `$bad_scanners` need to change over time.

---

## Managing the List

Recommended list name:

```
bad_scanners
```

Recommended sources:

- Cloudflare Security Events
- WAF Events
- Server access logs
- Honeypot hits
- Threat intelligence feeds

Only add IPs that have demonstrated malicious behavior.

Avoid adding IPs based on a single request.

---

## False Positives

Very Low

Because this rule blocks individual IP addresses, it should only include confirmed malicious hosts.

If an IP is no longer abusive, remove it from the Cloudflare List instead of disabling the rule.

---

## Change History

### v2026.07.1

Initial release.
