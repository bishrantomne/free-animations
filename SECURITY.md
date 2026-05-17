# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please **do not** open a public issue.  
Instead, open a **private security advisory** on this repository (GitHub → Security → Advisories → New draft) and include:

- A description of the vulnerability
- Steps to reproduce it
- Any potential impact

You will receive a response within **72 hours**. If the issue is confirmed, a fix will be prioritised and you will be credited (unless you prefer to remain anonymous).

---

## Fair Use & Abuse Prevention

This repository serves lightweight, static HTML animations. To keep it accessible for everyone:

- **Do not** send automated high-frequency requests (scraping loops, stress tests, bots) against any hosted version of these files.
- **Do not** use this project as a vector for DDoS amplification or resource exhaustion attacks.
- **Do not** attempt to exploit GitHub's infrastructure through this repository.

Abusive traffic patterns will be reported to the relevant hosting provider and, where applicable, to GitHub Trust & Safety.

---

## Responsible Disclosure

We follow a **90-day responsible disclosure** window. If a reported issue is not resolved within 90 days, you are free to publish your findings publicly, with prior notice to us.

---

## Scope

| In scope | Out of scope |
|---|---|
| XSS or code injection in HTML files | GitHub platform bugs (report to GitHub) |
| Malicious dependencies (if added in future) | Social engineering attempts |
| Data exposure in any future backend | Physical security |

---

## Rate Limiting Guidance (for hosted deployments)

If you fork and self-host these animations, we strongly recommend:

- Enabling rate limiting at the CDN or reverse-proxy level (e.g. Cloudflare, Nginx `limit_req`)
- Setting `Cache-Control` headers to reduce origin hits
- Blocking known bad-actor IP ranges via a WAF

This project itself is static and carries no server-side risk, but downstream deployments should take these precautions.
