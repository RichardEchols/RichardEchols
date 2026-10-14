# Richard Echols

**Applied AI Engineer · Founder of RMDW · Builder of the Jah private LLM platform**

I build AI systems end to end and run them in production: model serving on my own GPUs, the API gateway in front of it, the agent products on top, and the customer deployments that use them.

## Jah: a private LLM platform

- **7 production model generations** shipped June to September 2026, each promoted through an eval gate with one-command rollback.
- Served on **4x NVIDIA RTX PRO 6000 Blackwell** with SGLang: 1M-token context, vision, tool calling, up to **1,354 tokens/sec** aggregate.
- **Time to first token cut from 33 s to 0.33 s** with FP8 KV cache, chunked prefill and priority scheduling; speculative decoding took single-stream decode from about 40 to 92.8 tok/s.
- **Public benchmark:** pass@1 with hidden unit tests in a sandbox. Jah scores 19/20, tying Claude Opus 5 and GPT-5.6, and publishes the tasks it loses. → [kiyomibot.ai/benchmarks](https://kiyomibot.ai/benchmarks)
- **13 open-weight models** on Hugging Face, about 2,000 downloads. → [huggingface.co/RMDWLLC](https://huggingface.co/RMDWLLC)

## The gateway

One endpoint that speaks **OpenAI Chat Completions, Anthropic Messages and OpenAI Responses**, so Claude Code, Codex and Claude Desktop work against it with no changes. Hashed keys, metering, per-key concurrency guards, priority lanes and three-tier health-checked failover. Paying customers get a key with no human in the loop.

## Products

| Product | What it is |
|---|---|
| **KiyomiKode Desktop** | Signed, notarized macOS agent app on the Claude Agent SDK. 60+ releases, background computer use, Chrome control, 55 connectors, 548-test release gate. [Releases](https://github.com/RichardEchols/kiyomikode-desktop-releases) |
| **Kiyomi** | AI platform for businesses: agents, artifacts, private document search, connectors. 2,000+ users. [kiyomibot.ai](https://kiyomibot.ai) |
| **RMDW Academy** | Claude-written, rubric-graded AI lessons tailored to each business. [rmdw.ai](https://rmdw.ai) |
| **Second Key** | Claude Code plugin and MCP server that blocks risky agent actions. [secondkey.ai](https://secondkey.ai) |

Product source is private. The public showcase repos below document architecture and scope.

## Showcase repos

[kiyomi-777-showcase](https://github.com/RichardEchols/kiyomi-777-showcase) · [kiyomikode-showcase](https://github.com/RichardEchols/kiyomikode-showcase) · [kaiju-coder-showcase](https://github.com/RichardEchols/kaiju-coder-showcase) · [super-kaiju](https://github.com/RichardEchols/super-kaiju) · [rmdw-ai-systems-portfolio](https://github.com/RichardEchols/rmdw-ai-systems-portfolio)

## Stack

**Inference:** SGLang, vLLM, llama.cpp, MLX distributed, speculative decoding, FP8 / FP4 / NVFP4 / GGUF, LoRA fine-tuning
**Agents:** Claude Agent SDK, Anthropic and OpenAI APIs, MCP, tool use, computer use, RAG (pgvector, BM25)
**Platform:** Python, TypeScript, Next.js, React, Swift, Electron, Cloudflare Workers, Vercel, Neon Postgres, Stripe, Docker, Ubuntu

## Background

Enterprise and public sector before RMDW: a $1.6M ARR AI and FinOps portfolio at IBM, TBM analytics for a $7B IRS IT portfolio, and today Claude-assisted analytics and Power Platform automation for federal health IT leadership. M.S. Mathematics.

## Links

[rmdw.ai](https://rmdw.ai) · [LinkedIn](https://www.linkedin.com/in/richard-echols/) · [YouTube @RichardBEchols](https://www.youtube.com/@RichardBEchols) · [Hugging Face](https://huggingface.co/RMDWLLC)
