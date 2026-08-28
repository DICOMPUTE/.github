## What and why

<!-- What changed, and the reason behind it. The "why" is the part a reviewer
     cannot reconstruct from the diff. -->

Closes #

## How it was verified

<!-- The test you added, the gate you ran, or the manual steps. A fix without a
     regression test tends to come back. -->

- [ ] Added or updated a test that fails without this change
- [ ] Repository gates pass locally

## Risk

<!-- Delete the rows that don't apply. -->

| Area | Touched? |
|---|---|
| Metering / billing / ledger / settlement | no |
| Authentication, authorization, or key handling | no |
| Trust boundary between coordinator, gateway, and worker | no |
| Public API shape (breaking change) | no |

<!-- If any row is "yes", say which invariant is preserved and which test proves it. -->

## Checklist

- [ ] One concern per PR
- [ ] Style matches the surrounding code
- [ ] No secrets, keys, or internal hostnames in the diff or its tests
- [ ] This is not a security vulnerability disclosure (those go through [SECURITY.md](https://github.com/DICOMPUTE/.github/blob/main/SECURITY.md))
