# Awesome AI Sandboxes

A curated list of cloud sandbox and environment providers for AI agents.

All information is sourced exclusively from official documentation, landing pages, and GitHub repos. PRs welcome -- but please link to official sources only.

> **Why this list?** There's a lot of noise and inaccurate info about sandbox providers floating around online. This repo exists to fix that -- every claim here links back to the provider's own docs or landing page.

![Awesome AI Sandboxes Market Map](assets/market-map.png)

## Table of Contents

- [Code Execution & Full Environment Sandboxes](#code-execution--full-environment-sandboxes)
- [Browser Sandboxes](#browser-sandboxes)
- [Contributing](#contributing)

---

## Code Execution & Full Environment Sandboxes

### [E2B](https://e2b.dev)

Open-source, secure cloud sandboxes for AI agents with real-world tools. Powered by Firecracker microVMs.

- **Isolation:** Firecracker microVMs
- **Key features:** Code interpreter SDK, custom sandbox templates, desktop sandboxes (computer use), up to 24h sessions, filesystem & network access, sub-200ms cold starts
- **Stateful:** Yes -- persistent full environments, not just code execution
- **SDKs:** Python, JavaScript/TypeScript
- **Open source:** Yes -- [github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B) (Apache 2.0)
- **Self-hostable:** Yes (BYOC, on-prem)
- **Pricing:** Free tier available, pay-as-you-go

| Links |  |
|-------|--|
| Website | [e2b.dev](https://e2b.dev) |
| Docs | [e2b.dev/docs](https://e2b.dev/docs) |
| GitHub | [github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B) |

---

### [Daytona](https://daytona.io)

Secure and elastic infrastructure for running AI-generated code. Sub-90ms sandbox creation.

- **Isolation:** Secure isolated runtimes
- **Key features:** Sub-90ms creation, massive parallelization, file/git/LSP/execute APIs, environment snapshots, computer use (Linux, macOS, Windows), Docker-in-Docker support, volumes for shared data
- **Stateful:** Yes -- sandboxes run indefinitely, built for long-running and persistent agents
- **SDKs:** Python, TypeScript
- **Open source:** Yes -- [github.com/daytonaio/daytona](https://github.com/daytonaio/daytona)
- **Self-hostable:** Yes (customer-managed compute, on-prem)
- **Pricing:** Pay-as-you-go per second, $200 free compute included

| Links |  |
|-------|--|
| Website | [daytona.io](https://daytona.io) |
| Docs | [daytona.io/docs](https://daytona.io/docs) |
| GitHub | [github.com/daytonaio/daytona](https://github.com/daytonaio/daytona) |

---

### [Modal](https://modal.com)

Serverless cloud platform for AI with sandboxes, GPU compute, and sub-second cold starts.

- **Isolation:** Sandboxes with ephemeral isolated environments
- **Key features:** Pay-per-second billing, GPU support (H100, A100, L40S, etc.), sub-second container boots, autoscale 0 to 1000+ GPUs, SOC2 & HIPAA compliant
- **Stateful:** Sandboxes are ephemeral; volumes available for persistence
- **SDKs:** Python (primary), TypeScript/Go via libmodal
- **Open source:** SDK client is open source -- [github.com/modal-labs/modal-client](https://github.com/modal-labs/modal-client). Platform is closed-source.
- **Self-hostable:** No
- **Pricing:** Pay-as-you-go, $30/month free credits on Starter plan

| Links |  |
|-------|--|
| Website | [modal.com](https://modal.com) |
| Docs | [modal.com/docs](https://modal.com/docs) |
| GitHub | [github.com/modal-labs](https://github.com/modal-labs) |

---

### [Runloop](https://runloop.ai)

Devbox infrastructure for building, benchmarking, and shipping AI coding agents at enterprise scale.

- **Isolation:** Micro-VM sandboxes on custom bare-metal hypervisor
- **Key features:** 2x faster vCPUs, sub-2s startup for 10GB images, 10k+ parallel sandboxes, snapshot/branch state (Git for Agent State), suspend & resume, built-in SWE-Bench
- **Stateful:** Yes -- snapshot and branch sandbox state
- **SDKs:** Python, TypeScript
- **Open source:** SDK clients are open source. Platform is closed-source.
- **Self-hostable:** Deploy-to-VPC option available
- **Pricing:** Free tier with $50 credits, usage-based compute

| Links |  |
|-------|--|
| Website | [runloop.ai](https://runloop.ai) |
| Docs | [docs.runloop.ai](https://docs.runloop.ai) |
| GitHub | [github.com/runloopai](https://github.com/runloopai) |

---

### [CodeSandbox](https://codesandbox.io)

Cloud sandbox platform (now part of Together AI) for spinning up isolated microVM environments for AI agents.

- **Isolation:** MicroVM-based sandboxes
- **Key features:** Snapshot/restore in <2s, VM cloning in <2s, millions of concurrent VMs, customizable hibernation, forking for A/B testing agents, SOC 2 Type II
- **Stateful:** Yes -- snapshot and restore
- **SDKs:** TypeScript/JavaScript (`@codesandbox/sdk`)
- **Open source:** SDK is open source -- [github.com/codesandbox/codesandbox-sdk](https://github.com/codesandbox/codesandbox-sdk)
- **Self-hostable:** No
- **Pricing:** Free tier (40h VM credits/month), Scale from $170/month

| Links |  |
|-------|--|
| Website | [codesandbox.io](https://codesandbox.io) |
| Docs | [codesandbox.io/docs](https://codesandbox.io/docs) |
| GitHub | [github.com/codesandbox](https://github.com/codesandbox) |

---

### [OpenComputer](https://opencomputer.dev)

Persistent cloud VMs for AI agents by Digger. Full Linux machines that hibernate when idle and wake in seconds.

- **Isolation:** Full VMs with own filesystem, network, and process space
- **Key features:** Always-on persistent VMs, elastic compute (resize CPU/memory at runtime), hibernate & wake, instant checkpoints (snapshot/fork/rollback), 20GB disk per VM
- **Stateful:** Yes -- state survives across sessions, VMs stay alive until explicitly stopped
- **SDKs:** API-based (works with Claude Agent SDK and others)
- **Open source:** Yes -- [github.com/diggerhq/opencomputer](https://github.com/diggerhq/opencomputer)
- **Self-hostable:** Not specified
- **Pricing:** Pay-per-minute, pre-booked ($0.024/h) or instant ($0.12/h) for 2GB/1vCPU

| Links |  |
|-------|--|
| Website | [opencomputer.dev](https://opencomputer.dev) |
| Docs | [docs.opencomputer.dev](https://docs.opencomputer.dev) |
| GitHub | [github.com/diggerhq/opencomputer](https://github.com/diggerhq/opencomputer) |

---

### [Morph](https://morph.so)

Cloud infrastructure for AI agents with instant environment branching and burst scalability.

- **Isolation:** Full VM instances (not containers)
- **Key features:** Instant environment branching and snapshot/restore, burst scalability (millisecond deploys), used for SWE-Bench, RL rollouts, and computer-use agents
- **Stateful:** Yes -- snapshot and restore
- **SDKs:** Python, TypeScript
- **Open source:** SDKs are open source -- [github.com/morph-labs](https://github.com/morph-labs)
- **Self-hostable:** Not specified
- **Pricing:** Not publicly listed

| Links |  |
|-------|--|
| Website | [morph.so](https://morph.so) |
| GitHub | [github.com/morph-labs](https://github.com/morph-labs) |

---

### [Fly.io Machines](https://fly.io)

Hardware-virtualized micro VMs that launch in subseconds with per-second billing across 18+ global regions.

- **Isolation:** Hardware-virtualized VMs (Firecracker-based)
- **Key features:** Subsecond start/stop, Sprites (hardware-isolated sandboxes for AI code with checkpointing), 18+ global regions, REST API and CLI, built-in private networking
- **Stateful:** Yes -- persistent volumes and Sprites with checkpointing
- **SDKs:** REST API (language-agnostic), CLI (`flyctl`)
- **Open source:** No (platform is closed-source)
- **Self-hostable:** No
- **Pricing:** Pay-as-you-go per second, from ~$2/month for smallest VM

| Links |  |
|-------|--|
| Website | [fly.io](https://fly.io) |
| Docs | [fly.io/docs](https://fly.io/docs) |
| GitHub | [github.com/superfly](https://github.com/superfly) |

---

### [OpenSandbox](https://open-sandbox.ai) (by Alibaba)

Open-source, production-grade sandbox runtime for AI agents. Apache 2.0 license.

- **Isolation:** Docker/Kubernetes runtimes
- **Key features:** Unified sandbox APIs, supports coding agents, GUI agents, agent evaluation, AI code execution, and RL training
- **Stateful:** Not specified
- **SDKs:** Not specified
- **Open source:** Yes -- [github.com/alibaba/OpenSandbox](https://github.com/alibaba/OpenSandbox) (Apache 2.0)
- **Self-hostable:** Yes (self-hosted by design)
- **Pricing:** Free (open source)

| Links |  |
|-------|--|
| Website | [open-sandbox.ai](https://open-sandbox.ai) |
| GitHub | [github.com/alibaba/OpenSandbox](https://github.com/alibaba/OpenSandbox) |

---

## Browser Sandboxes

### [Browserbase](https://browserbase.com)

Headless browser infrastructure that gives AI agents reliable, scalable access to the web.

- **Key features:** Cloud browser sessions, Stagehand SDK for AI browser automation (22k+ GitHub stars), auto CAPTCHA solving, stealth mode, proxy support, session recording, supports Playwright/Puppeteer/Selenium
- **SDKs:** TypeScript/JavaScript (primary), Python, Go, Ruby, and more
- **Open source:** Stagehand SDK is open source -- [github.com/browserbase/stagehand](https://github.com/browserbase/stagehand). Platform is closed-source.
- **Pricing:** Free tier (1 browser hour), Developer $20/month, Startup $99/month

| Links |  |
|-------|--|
| Website | [browserbase.com](https://browserbase.com) |
| Docs | [docs.browserbase.com](https://docs.browserbase.com) |
| GitHub | [github.com/browserbase](https://github.com/browserbase) |

---

### [Steel](https://steel.dev)

Open-source browser API for AI agents with anti-detection, session management, and CAPTCHA solving.

- **Key features:** Session management with cookie/state persistence, up to 24h sessions, auto CAPTCHA solving, proxy support, compatible with Puppeteer/Playwright/Selenium, live session viewer
- **SDKs:** Python, Node.js/TypeScript
- **Open source:** Yes -- [github.com/steel-dev/steel-browser](https://github.com/steel-dev/steel-browser) (Apache 2.0, 7k+ stars)
- **Self-hostable:** Yes (Docker)
- **Pricing:** Free tier (Hobby), Starter $29/month, Developers $99/month

| Links |  |
|-------|--|
| Website | [steel.dev](https://steel.dev) |
| GitHub | [github.com/steel-dev/steel-browser](https://github.com/steel-dev/steel-browser) |

---

### [Scrapybara](https://scrapybara.com)

Virtual desktop infrastructure for AI computer-use agents -- Ubuntu, browser, and Windows instances.

- **Key features:** Ubuntu/browser/Windows instance types, Act SDK for unified computer-use model interface, session persistence (pause/resume), interactive streaming, supports OpenAI CUA and Claude computer use
- **SDKs:** Python, TypeScript
- **Open source:** Partially -- [github.com/Scrapybara/scrapybara-oss](https://github.com/Scrapybara/scrapybara-oss) (Apache 2.0)
- **Pricing:** Free tier (10 compute hours), Basic $29/month, Pro $99/month

| Links |  |
|-------|--|
| Website | [scrapybara.com](https://scrapybara.com) |
| GitHub | [github.com/Scrapybara](https://github.com/Scrapybara) |

---

## Contributing

Want to add a provider or fix an error? Please open a PR with a link to the provider's official documentation or landing page as the source.

**Rules:**
1. All information must come from official sources (docs, landing pages, official GitHub repos)
2. No blog posts, tweets, or third-party articles as primary sources
3. Keep entries factual -- no marketing fluff
4. Maintain alphabetical order within each category

## License

[CC BY-NC-SA 4.0](LICENSE.md)
