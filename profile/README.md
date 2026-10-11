<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-lockup.svg">
    <img src="./assets/logo-lockup-light.svg" alt="DiCompute" width="320">
  </picture>
</p>

<h3 align="center">Use AI. Share your GPU. Earn from AI compute.</h3>

<p align="center">
  Open AI models through one OpenAI-compatible API, served by independent GPU providers.<br>
  Usage is metered in micro-USD and settled on the XDC network.
</p>

<p align="center">
  <a href="https://dicompute.ai"><img alt="Website" src="https://img.shields.io/badge/website-dicompute.ai-245cff?style=flat-square"></a>
  <a href="https://dicompute.ai/docs"><img alt="Docs" src="https://img.shields.io/badge/docs-quickstart-245cff?style=flat-square"></a>
  <a href="https://github.com/DICOMPUTE/openapi"><img alt="OpenAPI 3.1" src="https://img.shields.io/badge/OpenAPI-3.1-245cff?style=flat-square"></a>
  <a href="https://dicompute.ai/status"><img alt="Status" src="https://img.shields.io/badge/status-dicompute.ai%2Fstatus-245cff?style=flat-square"></a>
  <a href="https://x.com/dicomputeai"><img alt="X" src="https://img.shields.io/badge/follow-%40dicomputeai-0b1020?style=flat-square&logo=x"></a>
</p>

<p align="center">
  <a href="https://dicompute.ai/console">Console</a> ·
  <a href="https://dicompute.ai/docs">Docs</a> ·
  <a href="https://dicompute.ai/models">Models</a> ·
  <a href="https://dicompute.ai/pricing">Pricing</a> ·
  <a href="https://dicompute.ai/status">Status</a> ·
  <a href="https://dicompute.ai/stats">Live stats</a> ·
  <a href="https://dicompute.ai/earn">Earn</a> ·
  <a href="https://dicompute.ai/changelog">Changelog</a> ·
  <a href="https://dicompute.ai/whitepaper">Whitepaper</a> ·
  <a href="https://dicompute.ai/brand">Brand</a>
</p>

---

## What DiCompute does

- **For developers:** one OpenAI-compatible endpoint for open AI models. You pay per token. There is no subscription.
- **For GPU owners:** you connect a GPU, serve requests through the same metered path, and earn for the capacity you already own.
- **For both:** usage is counted in integer micro-USD (µUSD) and settled on the XDC network, so the meter and the payout can be checked.

## Start in two minutes

1. Get an API key. Sign in at [dicompute.ai/console](https://dicompute.ai/console), or mint a key with one call:

   ```bash
   curl -sS -X POST https://dicompute.ai/api/signup \
     -H 'content-type: application/json' \
     -d '{"email":"you@example.com"}'
   # => {"apiKey":"sk-dico-...", ...}
   ```

   > The API shows the key **one time only**. Copy it now. There is no recovery flow.

2. Find a model id. The model list is live, so read it from the API:

   ```bash
   curl -sS https://dicompute.ai/openai/v1/models
   ```

3. Send a request:

   ```bash
   curl -sS -N https://dicompute.ai/openai/v1/chat/completions \
     -H "authorization: Bearer $DICO_KEY" \
     -H 'content-type: application/json' \
     -d '{"model":"qwen2.5-3b-instruct","stream":true,
          "messages":[{"role":"user","content":"say OK"}]}'
   ```

Do you use the OpenAI SDK already? Change two lines:

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://dicompute.ai/openai/v1",
    api_key="sk-dico-...",
)
```

The full contract is an OpenAPI 3.1 spec in **[DICOMPUTE/openapi](https://github.com/DICOMPUTE/openapi)**. Use it with Postman, Insomnia or any code generator.

## Models and prices

Models and prices change. This page does not copy them, so it cannot go out of date.

- Current models, capabilities and per-token prices: [dicompute.ai/models](https://dicompute.ai/models)
- The same data as JSON: [`/openai/v1/models`](https://dicompute.ai/openai/v1/models)
- How billing works: [dicompute.ai/pricing](https://dicompute.ai/pricing)

## Run a GPU and earn

Connect a GPU, serve traffic and claim earnings for each settlement epoch.

→ [Earn](https://dicompute.ai/earn) · [Operate a provider](https://dicompute.ai/operate) · [Leaderboard](https://dicompute.ai/leaderboard)

## Repositories

| Repository | What it is |
|---|---|
| **[openapi](https://github.com/DICOMPUTE/openapi)** | The OpenAPI 3.1 spec for the inference API, with curl, Python and TypeScript quickstarts |
| [blog](https://github.com/DICOMPUTE/blog) | The posts on [dicompute.ai/blog](https://dicompute.ai/blog), one markdown file per post |
| [Open](https://github.com/DICOMPUTE/Open) | Public feature issues, with the issue template we use for them |
| [.github](https://github.com/DICOMPUTE/.github) | This profile, and the organization's security, contributing and support policies |

Product engineering happens in private repositories. The public surface is the running service and the contract above.

## Get help

- Questions and support: [SUPPORT.md](https://github.com/DICOMPUTE/.github/blob/main/SUPPORT.md) · [hello@dicompute.ai](mailto:hello@dicompute.ai)
- Contributing: [CONTRIBUTING.md](https://github.com/DICOMPUTE/.github/blob/main/CONTRIBUTING.md) · [Code of Conduct](https://github.com/DICOMPUTE/.github/blob/main/CODE_OF_CONDUCT.md)

## Security

We do not take action against researchers who act in good faith.

- **Report privately:** open a draft advisory under a repository's **Security → Report a vulnerability**, or send an email to **security@dicompute.ai**.
- **Do not** open a public issue for a vulnerability.
- Full policy: [SECURITY.md](https://github.com/DICOMPUTE/.github/blob/main/SECURITY.md)

<p align="center">
  <img src="./assets/logo-mark.svg" alt="" width="32"><br>
  <sub>Settled on <a href="https://xinfin.org">XDC</a> · <a href="https://dicompute.ai/privacy">Privacy</a> · <a href="https://dicompute.ai/terms">Terms</a> · <a href="https://dicompute.ai/brand">Brand assets</a></sub>
</p>
