# Contributing to Awesome AI Sandboxes

This list aims to be the canonical factual reference for AI agent sandbox providers. Consistency and source rigor matter more than volume.

## Scope

**In scope:**
- Code execution sandboxes (microVMs, containers, gVisor, etc.)
- Browser sandboxes for AI agents
- Desktop / computer-use sandboxes
- Self-hostable sandbox orchestrators

**Out of scope:**
- Model hosts (Anthropic, OpenAI, AWS Bedrock, etc.)
- Pure GPU rental without sandbox/isolation positioning (vast.ai, RunPod, Lambda Labs)
- Orchestration-only tools without sandboxing (Composio, AgentOps, LangSmith)
- IDE/editor sandboxes positioned at end users, not agents

If you're unsure, open an issue before drafting a PR.

## Source rules

1. All claims must come from **official sources only** — the provider's docs, landing page, or official GitHub repo.
2. No blog posts, third-party articles, tweets, or marketing collateral as primary sources.
3. Keep entries factual — no marketing language, no superlatives, no comparisons to other providers.

Examples:
- ✅ "Sub-200ms cold starts" sourced from e2b.dev/docs
- ✅ "Apache 2.0" sourced from the GitHub LICENSE file
- ❌ "The fastest sandbox provider"
- ❌ "TechCrunch reported $50M Series A"

## Section placement

| License | Section |
|---|---|
| Apache 2.0, MIT, AGPL, BSD, MPL (any OSI-approved license) | **Open Source** |
| Proprietary, closed-source, source-available with restrictions | **Closed Source** |

Within each section, append new entries at the bottom.

## Entry template

Every entry needs the 8 required fields in this exact order. The 3 fields marked *(recommended)* should be included if the data is in the provider's docs.

````markdown
### [Name](https://provider.dev)
[Website](https://provider.dev) | [Docs](https://docs.provider.dev) | [GitHub](https://github.com/org/repo)

One- or two-sentence factual description. ≤ 25 words. Should tie to the sandbox theme.

- **Isolation:** {tech}
- **Key features:** {comma-separated list, 5–8 distinctive items}
- **Cold start:** {recommended — e.g., "<200ms", "Sub-90ms", "~25ms", or "Not specified"}
- **Max session:** {recommended — e.g., "24h", "Unlimited", "5h", or "Not specified"}
- **Snapshots / Forking:** {recommended — "Yes (snapshot + fork)" / "Yes (snapshot only)" / "No" / "Not specified"}
- **Stateful:** {Yes / Yes (with volumes) / Ephemeral / No / Not specified}
- **GPU:** {Yes (model list) / Yes / No / Not specified}
- **BYOC / Self-host:** {Yes / Yes (Enterprise) / Yes (deploy-to-VPC) / No / Not specified}
- **SDKs:** {languages, with package names in backticks}
- **License:** {Apache 2.0 / MIT / AGPL 3.0 / etc. — required for Open Source section}
- **Pricing:** {free tier description; paid model; starting price}

---
````

## Standardized values

To keep entries comparable, use these enums where applicable.

**Stateful:** `Yes` / `Yes (with volumes)` / `Ephemeral` / `No` / `Not specified`

**GPU:** `Yes (<model list>)` / `Yes` / `No` / `Not specified`

**BYOC / Self-host:** `Yes` / `Yes (Enterprise)` / `Yes (deploy-to-VPC)` / `No` / `Not specified`

**Snapshots / Forking:** `Yes (snapshot + fork)` / `Yes (snapshot only)` / `No` / `Not specified`

## Description guidelines

- ≤ 25 words, 1–2 sentences
- Ties to "sandbox" or related vocabulary
- States what the product IS, not what it's better than

Good: "Open-source browser API for AI agents and apps. Sandboxed Chrome sessions with anti-detection, session viewer, and computer-use integrations."

Bad: "The fastest, most secure browser sandbox ever built."

## Submission checklist

- [ ] Entry placed in correct section (license-based)
- [ ] Field order matches template exactly
- [ ] All 8 required fields present
- [ ] All 3 recommended fields included if data is available
- [ ] All claims link to official sources
- [ ] Description ≤ 25 words and ties to the sandbox theme
- [ ] Trailing `---` separator included
- [ ] PR title: `Add <Name>`
- [ ] PR body links to the official sources used

## Review criteria

PRs are reviewed for:

1. **Source verification** — every factual claim traces to an official source
2. **Template compliance** — field order, formatting, section placement
3. **Scope** — in/out per the scope section above
4. **Factual neutrality** — no marketing language, no comparative claims

## Field design notes

The following attributes were considered as top-level fields and deliberately kept inside **Key features** as free text instead. Future contributors are welcome to propose promoting them via a separate issue if the case strengthens.

| Considered | Rationale for not promoting to a top-level field |
|---|---|
| Compliance / certifications (SOC 2, HIPAA, ISO 27001) | Mostly negotiated per-contract, rarely a public-tier feature. Remains valid inside Key features when officially advertised. |
| Max concurrency | Overlaps with provider-specific scale claims already captured in Key features (50k+ sandboxes, millions of VMs, etc.). |
| Resources per sandbox (CPU / RAM / disk) | Varies by plan tier; not a fixed comparable. |
| Computer use / desktop support | Binary field would miss nuance (Linux-only vs cross-OS vs browser-only). Stays in Key features as text. |
