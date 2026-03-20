# Contributing to Awesome AI Auth

Thanks for helping keep this list sharp. This is maintained by engineers actively working in AI security — contributions that reflect real-world deployment experience are especially welcome.

## What belongs here

A tool belongs on this list if it:

- Directly addresses credential security, secrets management, or authentication for AI agents / LLM systems
- Is actively maintained (last commit within 12 months, or has a stable release)
- Has public documentation or a working demo

**Deterministic tools** (credential never reaches the LLM) are listed first. If you're adding something probabilistic (classifier, scanner, etc.), be honest about what it can and can't guarantee.

## What doesn't belong

- Generic DevSecOps tools with no AI-specific angle
- Unmaintained or vaporware projects
- Tools you built yourself without any external usage/validation (conflict of interest — ask someone else to submit it)

## How to add a tool

1. Fork the repo and create a branch: `git checkout -b add/<tool-name>`
2. Add your entry to `README.md` in the appropriate section, following the format below
3. Open a PR with a one-line description of why the tool belongs here

### Entry format

```markdown
- **[Tool Name](https://github.com/org/repo)** ![](https://img.shields.io/github/stars/org/repo?style=flat-square&label=☆) — One sentence: what problem it solves and why it's deterministic/probabilistic. [Relevant doc or guide](https://link).
```

For non-GitHub tools (commercial, research papers):

```markdown
- **[Tool Name](https://link)** — One sentence description. [Supporting doc](https://link).
```

### Sections

| Section | What goes here |
|---------|---------------|
| Step 1: Keep Secrets Out of LLM Context | Credential brokers, isolation layers |
| Step 2: Use a Real Vault | Secrets platforms with dynamic tokens |
| Step 3: Give Agents Identities, Not Keys | Workload identity, OAuth, cryptographic auth |
| Step 4: Harden the Infrastructure | Sandboxes, network allowlists, OS-level controls |
| Step 5: Add Guardrails | Classifiers, scanners, audit tools |
| Benchmarks & Evaluation | Datasets, evaluation frameworks |
| Related Lists | Other curated lists in adjacent spaces |

## Fixing or updating existing entries

If a tool is abandoned, has a better link, or you want to add a relevant guide/blog post to an existing entry — just open a PR with the change and a brief explanation.

## Tone

This list takes a strong position: **deterministic > probabilistic > nothing**. PR descriptions that blur this distinction (e.g., claiming a classifier "prevents" injection) will be pushed back on. That's a feature, not a bug.

## Questions

Open an issue or ping the maintainers in the PR thread.
