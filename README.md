<div align="center">

# Awesome AI Auth

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![License](https://img.shields.io/badge/license-CC0--1.0-blue.svg)

**A curated list of tools and resources for securing AI agent authentication, credentials, and secrets.**

### [Browse the full site &rarr;](https://yayashuxue.github.io/awesome-ai-auth/)

</div>

---

## What's Inside

- **Threat Landscape** — 6 attack scenarios in plain English, not jargon
- **Interactive Checklist** — "Is your AI agent leaking?" Click to audit yourself
- **Deterministic vs. Probabilistic** — Which protections are mathematically guaranteed vs. best-effort
- **Agent Stack Breakdown** — How Claude Code, OpenClaw, and MCP actually handle credentials, line by line
- **Attack Chain Diagrams** — Mermaid sequence diagrams showing real exploit flows
- **30+ Tools** — Organized by category: vaults, detection, identity, guardrails, and more

## Categories

| Category | Examples |
|----------|----------|
| Infrastructure Hardening | [IronShell](https://github.com/Surfing-Claw/IronShell), [IronClaw](https://github.com/nearai/ironclaw) |
| Credential Managers | [AgentPassVault](https://github.com/joshua5201/AgentPassVault), [Vault-MCP](https://github.com/Chill-AI-Space/vault-mcp), [Mozilla any-llm](https://github.com/mozilla-ai/any-llm) |
| Secrets Detection | [GitGuardian ggshield](https://github.com/GitGuardian/ggshield), [Presidio](https://github.com/microsoft/presidio) |
| Secrets Management | [HashiCorp Vault](https://developer.hashicorp.com/validated-patterns/vault/ai-agent-identity-with-hashicorp-vault), [Infisical](https://github.com/Infisical/infisical), [1Password Agentic](https://1password.com/solutions/agentic-ai) |
| Agent Security Plugins | [SecureClaw](https://github.com/adversa-ai/secureclaw), [ClawSec](https://github.com/prompt-security/clawsec) |
| OAuth & Identity | [MCP Gateway Registry](https://github.com/agentic-community/mcp-gateway-registry), [Aembit](https://aembit.io/blog/securing-ai-agents-without-secrets/), [AgentGateway](https://www.solo.io/blog/aaif-announcement-agentgateway) |
| Prompt Injection Defense | [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails), [Llama Guard](https://github.com/meta-llama/PurpleLlama), [Guardrails AI](https://github.com/guardrails-ai/guardrails) |

## The Core Insight

```
DETERMINISTIC (guaranteed)          PROBABILISTIC (best-effort)         NO PROTECTION
─────────────────────────           ───────────────────────────         ─────────────
Credential broker                   Prompt injection classifier         "Never reveal
Network allowlist/firewall          Output secret scanner                secrets" in
WASM sandbox (no network)           LLM-based tool validator             system prompt
Auto-expiring tokens                PII redactor
Hard human-in-the-loop gate         Training data filter
Tool permission blocklist
```

> **If a credential is in the LLM's context window, no amount of prompt engineering can guarantee it won't leak. The only guarantee is architectural: don't put the secret in the context at all.**

## Contributing

PRs welcome! Please ensure entries include a link, brief description, and relevance to AI auth or credential protection.
