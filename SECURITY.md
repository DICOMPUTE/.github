# Security Policy

DiCompute operates a live money path: real API keys, real per-token metering, and
on-chain settlement. We treat security reports as first-class work and we will not
take legal action against researchers acting in good faith under this policy.

## Reporting a vulnerability

**Do not open a public issue for a vulnerability.**

| | How |
|---|---|
| **Preferred** | On the affected repository: **Security → Report a vulnerability**. GitHub keeps the advisory private between you and us. |
| **Email** | **security@dicompute.ai** |

Please include: what you found, where, how to reproduce it, and the impact you
believe it has. A working proof of concept helps us confirm and fix faster.

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement | 3 business days |
| Triage and severity assessment | 10 business days |
| Fix or documented mitigation | Tracked to closure, severity-dependent |

We will keep you updated as we work, and we are glad to credit you when the fix
ships — tell us how you'd like to be named, or if you'd rather stay anonymous.

## In scope

- **Authentication and authorization** — signup, API key handling, account takeover, privilege escalation
- **Money path** — metering, billing, ledger accounting, refunds, receipts, settlement correctness
- **Cryptography** — key derivation, session handling, transport sealing, signature verification
- **Input validation** — injection, deserialization, parsing, SSRF
- **Isolation** — sandbox escape, tenant boundary crossing, worker/coordinator trust boundaries
- **Availability** — resource exhaustion reachable by an unprivileged caller

## Out of scope

- Volumetric denial of service and load testing against production
- Social engineering of staff, operators, or users
- Findings that require a physically compromised or rooted operator machine, where our
  documented trust model already states the limitation
- Missing hardening headers with no demonstrated exploit path
- Automated scanner output with no analysis of reachability or impact
- Reports against third-party services we merely link to

## Ground rules

- Use your own accounts and test data. Do not access, modify, or retain data belonging to others.
- Do not degrade the service for real users.
- Give us reasonable time to remediate before public disclosure.

## Supported versions

DiCompute is continuously deployed. Only the currently deployed version receives
security updates — there are no maintained release branches.
