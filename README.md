# Awesome AI Sandboxes

A curated list of cloud sandbox providers for AI agents.

All information sourced exclusively from official docs and landing pages. PRs welcome, but please link to official sources only.

> **Why this list?** There's a lot of noise and inaccurate info about sandbox providers online. This repo exists to fix that. Every claim here links back to the provider's own docs or landing page.

![Awesome AI Sandboxes Market Map](assets/market-map.png)

---

## Open Source

### [E2B](https://e2b.dev)
[Website](https://e2b.dev) | [Docs](https://e2b.dev/docs) | [GitHub](https://github.com/e2b-dev/E2B) | stateful, self-host

Secure cloud sandboxes for AI agents with real-world tools. Powered by Firecracker microVMs.

- **Isolation:** Firecracker microVMs
- **Key features:** Code interpreter SDK, custom sandbox templates, desktop sandboxes (computer use), up to 24h sessions, filesystem & network access, sub-200ms cold starts
- **Stateful:** Yes, persistent full environments, not just code execution
- **GPU:** No
- **BYOC / Self-host:** Yes (BYOC, on-prem, self-hosted)
- **SDKs:** Python, JavaScript/TypeScript
- **License:** Apache 2.0
- **Pricing:** Free tier available, pay-as-you-go

---

### [Daytona](https://daytona.io)
[Website](https://daytona.io) | [Docs](https://daytona.io/docs) | [GitHub](https://github.com/daytonaio/daytona) | stateful, gpu, self-host

Secure and elastic infrastructure for running AI-generated code. Sub-90ms sandbox creation.

- **Isolation:** Secure isolated runtimes
- **Key features:** Sub-90ms creation, massive parallelization, file/git/LSP/execute APIs, environment snapshots, computer use (Linux, macOS, Windows), Docker-in-Docker, volumes for shared data
- **Stateful:** Yes, sandboxes run indefinitely, built for long-running and persistent agents
- **GPU:** Yes (Nvidia H100, RTX PRO 6000)
- **BYOC / Self-host:** Yes (customer-managed compute, on-prem)
- **SDKs:** Python, TypeScript
- **License:** Apache 2.0
- **Pricing:** Pay-as-you-go per second, $200 free compute included

---

### [OpenComputer](https://opencomputer.dev)
[Website](https://opencomputer.dev) | [Docs](https://docs.opencomputer.dev) | [GitHub](https://github.com/diggerhq/opencomputer) | stateful

Persistent cloud VMs for AI agents by Digger. Full Linux machines that hibernate when idle and wake in seconds.

- **Isolation:** Full VMs with own filesystem, network, and process space
- **Key features:** Always-on persistent VMs, elastic compute (resize CPU/memory at runtime), hibernate & wake, instant checkpoints (snapshot/fork/rollback), 20GB disk per VM
- **Stateful:** Yes, state survives across sessions, VMs stay alive until explicitly stopped
- **GPU:** No
- **BYOC / Self-host:** Not specified
- **SDKs:** API-based (works with Claude Agent SDK and others)
- **Pricing:** Pay-per-minute, pre-booked ($0.024/h) or instant ($0.12/h) for 2GB/1vCPU

---

### [OpenSandbox](https://open-sandbox.ai) (by Alibaba)
[Website](https://open-sandbox.ai) | [GitHub](https://github.com/alibaba/OpenSandbox) | self-host

Production-grade sandbox runtime for AI agents.

- **Isolation:** Docker/Kubernetes runtimes
- **Key features:** Unified sandbox APIs, supports coding agents, GUI agents, agent evaluation, AI code execution, and RL training
- **GPU:** Not specified
- **BYOC / Self-host:** Yes (self-hosted by design)
- **License:** Apache 2.0
- **Pricing:** Free (open source)

---

## Closed Source

### [Blaxel](https://blaxel.ai)
[Website](https://blaxel.ai) | [Docs](https://docs.blaxel.ai) | [GitHub](https://github.com/blaxel-ai) | stateful

The perpetual sandbox platform. Sandboxes auto-suspend when idle and resume from standby in ~25ms with full memory state.

- **Isolation:** Individual microVMs with root filesystem in memory
- **Key features:** 25ms resume from standby, auto-suspend to $0 compute, 50k+ concurrent sandboxes, Agent Drive (distributed filesystem), volumes for long-term data, agent + MCP server co-hosting on same backbone
- **Stateful:** Yes, full memory + filesystem snapshot on suspend, persists forever
- **GPU:** No
- **BYOC / Self-host:** No
- **SDKs:** TypeScript, Python
- **Pricing:** Pay for active compute only, $0 on standby. SOC 2, HIPAA, ISO 27001

---

### [Cloudflare Sandboxes](https://developers.cloudflare.com/sandbox/)
[Docs](https://developers.cloudflare.com/sandbox/) | [GitHub](https://github.com/cloudflare/sandbox-sdk) | [Blog](https://blog.cloudflare.com/sandbox-ga/) | stateful

Persistent, isolated environments powered by Cloudflare Containers. Full computer for AI agents with shell, filesystem, and background processes.

- **Isolation:** Containers (Cloudflare Containers)
- **Key features:** Snapshots with R2 storage, secure credential injection via egress proxy, PTY terminal support, persistent code interpreters, live preview URLs, filesystem watching, active CPU pricing (pay only for used cycles)
- **Stateful:** Yes, auto-sleep on idle and wake on request, snapshots for full disk state
- **GPU:** No
- **BYOC / Self-host:** No (runs on Cloudflare's network)
- **SDKs:** JavaScript/TypeScript (`@cloudflare/sandbox`)
- **Pricing:** Active CPU pricing, up to 15k concurrent instances on standard plan

---

### [CodeSandbox](https://codesandbox.io)
[Website](https://codesandbox.io) | [Docs](https://codesandbox.io/docs) | [GitHub](https://github.com/codesandbox) | stateful

Cloud sandbox platform (now part of Together AI) for isolated microVM environments for AI agents.

- **Isolation:** MicroVM-based sandboxes
- **Key features:** Snapshot/restore in <2s, VM cloning in <2s, millions of concurrent VMs, customizable hibernation, forking for A/B testing agents, SOC 2 Type II
- **Stateful:** Yes, snapshot and restore
- **GPU:** No
- **BYOC / Self-host:** No
- **SDKs:** TypeScript/JavaScript (`@codesandbox/sdk`)
- **Pricing:** Free tier (40h VM credits/month), Scale from $170/month

---

### [Modal](https://modal.com)
[Website](https://modal.com) | [Docs](https://modal.com/docs) | [GitHub](https://github.com/modal-labs) | gpu

Serverless cloud platform for AI with sandboxes, GPU compute, and sub-second cold starts.

- **Isolation:** Sandboxes with ephemeral isolated environments
- **Key features:** Pay-per-second billing, sub-second container boots, autoscale 0 to 1000+ GPUs, SOC2 & HIPAA compliant
- **Stateful:** Sandboxes are ephemeral; volumes available for persistence
- **GPU:** Yes (H100, A100, L40S, A10, L4, T4, B200, H200)
- **BYOC / Self-host:** No
- **SDKs:** Python (primary), TypeScript/Go via libmodal
- **Pricing:** Pay-as-you-go, $30/month free credits on Starter plan

---

### [Morph](https://morph.so)
[Website](https://morph.so) | [GitHub](https://github.com/morph-labs) | stateful

Cloud infrastructure for AI agents with instant environment branching and burst scalability.

- **Isolation:** Full VM instances (not containers)
- **Key features:** Instant environment branching and snapshot/restore, burst scalability (millisecond deploys), used for SWE-Bench, RL rollouts, and computer-use agents
- **Stateful:** Yes, snapshot and restore
- **GPU:** Not specified
- **BYOC / Self-host:** Not specified
- **SDKs:** Python, TypeScript
- **Pricing:** Not publicly listed

---

### [Runloop](https://runloop.ai)
[Website](https://runloop.ai) | [Docs](https://docs.runloop.ai) | [GitHub](https://github.com/runloopai) | stateful, self-host

Devbox infrastructure for building, benchmarking, and shipping AI coding agents at enterprise scale.

- **Isolation:** Micro-VM sandboxes on custom bare-metal hypervisor
- **Key features:** 2x faster vCPUs, sub-2s startup for 10GB images, 10k+ parallel sandboxes, snapshot/branch state (Git for Agent State), suspend & resume, built-in SWE-Bench
- **Stateful:** Yes, snapshot and branch sandbox state
- **GPU:** Not specified
- **BYOC / Self-host:** Yes (deploy-to-VPC option)
- **SDKs:** Python, TypeScript
- **Pricing:** Free tier with $50 credits, usage-based compute

---

### [Sprites](https://sprites.dev) (by Fly.io)
[Website](https://sprites.dev) | [Docs](https://docs.sprites.dev) | [API](https://sprites.dev/api) | stateful

Persistent, hardware-isolated execution environments. A Sprite is a full Linux computer with stateful filesystem, unlimited checkpoints, and granular billing.

- **Isolation:** Firecracker VMs with isolated networking
- **Key features:** Persistent ext4 filesystem across runs, live checkpoints (~300ms, copy-on-write), dynamic resources (up to 8 CPUs / 16GB RAM), HTTP access with unique URLs per Sprite, L3 network egress policies, auto-activate on request
- **Stateful:** Yes, filesystem persists between runs, full environment checkpointed
- **GPU:** No
- **BYOC / Self-host:** No
- **SDKs:** JavaScript, Go, CLI, REST API
- **Pricing:** Pay for actual usage: $0.07/CPU-hour, $0.04375/GB-hour memory, $30 trial credits

---

## Contributing

Want to add a provider or fix an error? Open a PR with a link to the provider's official documentation or landing page as the source.

**Rules:**
1. All information must come from official sources (docs, landing pages, official GitHub repos)
2. No blog posts, tweets, or third-party articles as primary sources
3. Keep entries factual, no marketing fluff

## License

[CC BY-NC-SA 4.0](LICENSE.md)
