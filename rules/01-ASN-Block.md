# Rule 01 - ASN Block

## Purpose

Block requests originating from known malicious Autonomous System Numbers (ASN).

This rule is designed to stop abusive hosting providers, bulletproof VPS networks, and repeatedly observed scanning infrastructure before they reach the application.

---

## Action

```
Block
```

---

## Cloudflare Expression

```cf
ip.geoip.asnum in {
48090
34343
210558
211298
202412
197170
25369
41608
202425
214481
}
```

---

## Rule Name

```
ASN Block
```

---

## Recommended Priority

```
1
```

This rule should be evaluated before all other custom rules.

---

## Why Block by ASN?

Blocking malicious ASN reduces:

- Vulnerability scanners
- Internet-wide crawlers
- Botnet traffic
- Mass exploitation attempts
- Credential stuffing infrastructure

before they consume additional WAF resources.

---

## Maintenance

Update this rule only when an ASN repeatedly appears in attack logs.

Avoid adding residential ISP ASNs unless there is clear evidence of abuse.

---

## False Positives

Very Low

ASN blocking affects every IP within the selected provider.

Always verify before adding new ASNs.

---

## Change History

### v2026.07.1

Initial release.
