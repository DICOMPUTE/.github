<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-lockup.svg">
    <img src="./assets/logo-lockup-light.svg" alt="DiCompute" width="320">
  </picture>
</p>

<p align="center">
  <strong>Decentralized AI inference on XDC.</strong><br>
  One OpenAI-compatible endpoint over independent GPU operators.<br>
  Micro-USD metering, on-chain settlement.
</p>

<p align="center">
  <a href="https://dicompute.ai"><img alt="Website" src="https://img.shields.io/badge/website-dicompute.ai-10141a?style=flat-square"></a>
  <a href="https://dicompute.ai/models"><img alt="API" src="https://img.shields.io/badge/API-OpenAI--compatible-2ce0a7?style=flat-square"></a>
  <a href="https://dicompute.ai/whitepaper"><img alt="Settlement" src="https://img.shields.io/badge/settlement-XDC-4de7ff?style=flat-square"></a>
  <a href="https://x.com/dicomputeai"><img alt="X" src="https://img.shields.io/badge/follow-%40dicompute-10141a?style=flat-square&logo=x"></a>
</p>

<p align="center">
  <a href="https://dicompute.ai">Website</a> ·
  <a href="https://dicompute.ai/console">Console</a> ·
  <a href="https://dicompute.ai/models">Models</a> ·
  <a href="https://dicompute.ai/whitepaper">Whitepaper</a> ·
  <a href="https://dicompute.ai/stats">Live stats</a> ·
  <a href="https://dicompute.ai/earn">Earn</a> ·
  <a href="https://dicompute.ai/brand">Brand</a>
</p>

---

## What we're building

AI inference reaches you through a stack of markups — chipmaker, hyperscaler,
API vendor. DiCompute routes it differently: a single OpenAI-compatible endpoint
in front of a network of **independent GPU operators**, with usage metered to the
**micro-USD** and settled **on the XDC network**.

You get one endpoint and per-token pricing. Operators get paid for capacity they
already own. Nobody has to trust an invoice — the meter and the settlement are
both auditable.

## Start in two minutes

No account, no password, no credit card. Signup mints a key and real starting credit.

```bash
# 1 — mint a key
curl -sS -X POST https://dicompute.ai/api/signup \
  -H 'content-type: application/json' \
  -d '{"email":"you@example.com"}'
# => {"apiKey":"sk-dico-...","account":"signup-...","startingBalanceUusd":100000}
```

> The key is returned **exactly once**. There is no recovery flow — copy it now.

```bash
# 2 — stream a completion
curl -sS -N https://dicompute.ai/openai/v1/chat/completions \
  -H "authorization: Bearer $DICO_KEY" \
  -H 'content-type: application/json' \
  -d '{"model":"qwen2.5-3b-instruct","stream":true,
       "messages":[{"role":"user","content":"say OK"}]}'
```

Already using the OpenAI SDK? Change two lines:

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://dicompute.ai/openai/v1",
    api_key="sk-dico-...",
)
```

## Live models

Queried from [`/openai/v1/models`](https://dicompute.ai/openai/v1/models) — always
resolve model ids from the API rather than hardcoding them.

| Model | Input / Mtok | Output / Mtok | Notes |
|---|---|---|---|
| `qwen2.5-3b-instruct` | $0.05 | $0.20 | General instruct |
| `medgemma-4b-it` | $0.05 | $0.20 | Vision-capable |
| `qwen2.5-0.5b-instruct` | $0.01 | $0.04 | Smallest / cheapest |

Billing is integer µUSD end to end — no floating-point drift between what the
router measures and what your balance is charged. See
[dicompute.ai/models](https://dicompute.ai/models) for current rates.

## Run a GPU and get paid

Idle accelerators earn. Operators join the fleet, serve traffic through the same
metered path, and claim earnings per epoch against on-chain settlement.

→ [dicompute.ai/earn](https://dicompute.ai/earn) · [dicompute.ai/operate](https://dicompute.ai/operate) · [dicompute.ai/leaderboard](https://dicompute.ai/leaderboard)

## Security

We take reports seriously and will not pursue researchers acting in good faith.

- **Report privately** — open a draft advisory under a repository's **Security → Report a vulnerability**, or email **security@dicompute.ai**.
- **Please don't** open a public issue for a vulnerability.
- Full policy: [SECURITY.md](https://github.com/DICOMPUTE/.github/blob/main/SECURITY.md)

## Around here

Most DiCompute engineering happens in private repositories. This organization's
public surface is the product itself — the console, the API, and the docs linked
above. Brand assets and usage rules live at [dicompute.ai/brand](https://dicompute.ai/brand).

<p align="center">
  <sub>Built on <a href="https://xinfin.org">XDC</a> · <a href="https://dicompute.ai/privacy">Privacy</a> · <a href="https://dicompute.ai/terms">Terms</a></sub>
</p>
