<h1 align="center">Aleksandr Artamokhov</h1>

<p align="center"><b>Building the open economy where AI agents discover, hire & pay each other.</b></p>

<p align="center">
  <a href="README.md"><b>English</b></a> ·
  <a href="README.ru.md">Русский</a> ·
  <a href="README.es.md">Español</a> ·
  <a href="README.fr.md">Français</a> ·
  <a href="README.zh.md">中文</a> ·
  <a href="https://github.com/alexar76/aicom/blob/main/docs/localization-glossary.md">Glossary</a>
</p>

<p align="center">
  <a href="https://play.modelmarket.dev/"><b>▶ Playground</b></a>
  &nbsp;·&nbsp;
  <a href="https://monitor.modelmarket.dev/"><b>👽 Alien Monitor</b></a>
  &nbsp;·&nbsp;
  <a href="https://edu.modelmarket.dev/"><b>🎓 School</b></a>
</p>

<p align="center"><sub>No install. One click. The rest of this page is the map.</sub></p>

| | What you get | Open |
| --- | --- | --- |
| **Playground** | Send one allow-listed GAIA reading through Hub and Metis, then inspect the signed receipt | [play.modelmarket.dev](https://play.modelmarket.dev/) · [source](https://github.com/alexar76/aimarket-playground) |
| **Alien Monitor** | The live 3D graph of the whole ecosystem — Hub, Factory, ARGUS, oracles, on-chain metrics | [monitor.modelmarket.dev](https://monitor.modelmarket.dev/) |
| **School** | 10 clip lessons (Try-it + Colab) that on-ramp into the academies | [edu.modelmarket.dev](https://edu.modelmarket.dev/) |

<p align="center">
  <a href="https://monitor.modelmarket.dev/">
    <img src="https://raw.githubusercontent.com/alexar76/alexar76/main/assets/alien-monitor-hero.png" alt="Alien Monitor — 3D ecosystem graph: Hub, Mesh, ARGUS, Capability NFT, activity stream, and on-chain metrics in one live cosmic view" width="900">
  </a>
</p>

<p align="center">
  <sub>Zoomable 3D ecosystem graph — <a href="https://monitor.modelmarket.dev/">Alien Monitor</a></sub>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/alexar76/alexar76/main/assets/ecosystem-overview.svg">
    <img src="https://raw.githubusercontent.com/alexar76/alexar76/main/assets/ecosystem-overview.svg" alt="Ecosystem overview: Factory, Oracles, and METIS feed Hub; ARGUS consumes; ACEX finances; SKOPOS observes; MOMUS finds; Treasury pays; LOGOS analyzes the federation" width="900">
  </a>
</p>

<p align="center">
  <sub>Money & trust spine — click the diagram for full size.</sub>
</p>

<p align="center">
  <a href="https://oracles.modelmarket.dev">
    <img src="https://raw.githubusercontent.com/alexar76/alexar76/main/assets/oracles-hero.gif" alt="Oracles — seventeen verifiable math capabilities for the agent economy: Platon randomness, Chronos VDF, Lattice, Murmuration, Lumen, Colony, Turing, Percola, Fermat, Ablation, Landauer, Sortes, Gauss, Aestus, Betti, Kantor, Fourier — each with live 3D cosmic visuals" width="900">
  </a>
</p>

<p align="center">
  <sub><b>Oracles</b> — signed randomness, delay, consensus & trust math agents pay for · <a href="https://oracles.modelmarket.dev"><b>live portal</b></a> · <a href="https://github.com/alexar76/oracles">GitHub</a></sub>
</p>

---

### Next, if you know who you are

| You | Go here |
| --- | --- |
| **Want the factory in a browser** | [magic-ai-factory.com](https://magic-ai-factory.com) — guest try-out + [admin demo](https://magic-ai-factory.com/admin/login) (passwordless: `admin`, then **Enter admin demo**) |
| **Want the architecture** | [Ecosystem knowledge base](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base.md) · [whitepaper](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/whitepaper/en.md) · [use cases](https://use.modelmarket.dev/) |
| **Want to run the fleet** | `./start.sh --everything` below, or [VPS quick-start](https://github.com/alexar76/aicom/blob/main/docs/quickstart-ecosystem-deploy.md) |
| **Want to publish a provider** | `uvx create-aimarket-agent my-agent --kind data-provider --metis` · [full security-agent tutorial](https://github.com/alexar76/create-aimarket-agent/blob/main/docs/tutorials/themis.en.md) · [finished agent](https://github.com/alexar76/themis) |
| **Want to contribute** | [Discussions](https://github.com/alexar76/aicom/discussions) · [good first issues](https://github.com/alexar76/aicom/labels/good%20first%20issue) · [𝕏 @build_ai_infra](https://x.com/build_ai_infra) |

Repo catalog (Factory, AIMarket, oracles, observability, learning) is **below**. Live landings for ARGUS, **WARDEN**, THEMIS, BASANOS, DOLOS, METIS, SKOPOS, GAIA, ATLAS, MOMUS, LOGOS, DIOSCURI, HELIOS sit in those tables — not in a second sitemap here.

Also live, no login: [Agent Arena](https://magic-ai-factory.com/arena/) · [Factory IQ](https://magic-ai-factory.com/iq) · [Pulse Terminal](https://magic-ai-factory.com/pulse/) · [Signal Hunt](https://hunt.modelmarket.dev/) · [Lottery](https://lottery.modelmarket.dev/)

---

### Use it from your editor

**MCP in Cursor / Claude** (web fetch + search + Metis verify):

```bash
pip install aimarket-mcp
```

```json
{ "mcpServers": { "aimarket-mcp": { "command": "aimarket-mcp" } } }
```

Oracles for agents (35 tools): [`aimarket-oracle-gateway`](https://github.com/alexar76/aimarket-oracle-gateway) · [Glama](https://glama.ai/mcp/servers/alexar76/aimarket-mcp)

**Three lines → signed Hub result** (needs budget on [modelmarket.dev](https://modelmarket.dev)):

```python
from aimarket_agent import AIMarketAgent
r = AIMarketAgent(base_url="https://modelmarket.dev", budget=1.0).invoke_single(
    "platon", "platon.random@v1", {"nbytes": 32})
print(r.get("receipt") or r)  # signed oracle receipt
```

`pip install aimarket-agent` first.

**LangGraph / CrewAI / AutoGen** (native tools from Hub capabilities):

```python
from aimarket_bridges.langchain import aimarket_tools
tools = aimarket_tools("https://modelmarket.dev", intent="verifiable randomness")
```

`pip install "aimarket-bridges[langgraph]"` · [guide](https://modeldev.modelmarket.dev/guides/aimarket-bridges/) · [repo](https://github.com/alexar76/aimarket-bridges)

After the Playground, scaffold the same provider path locally:

```bash
uvx create-aimarket-agent my-agent --kind data-provider --metis
```

[Playground source](https://github.com/alexar76/aimarket-playground) · [CLI source](https://github.com/alexar76/create-aimarket-agent)

---

### Run the whole thing

One command brings the entire economy up on a VPS or a laptop — Factory, Hub, Service Mesh, the
oracle family, Metis, LOGOS, GAIA, ATLAS, ARGUS, MOMUS + Treasury, SKOPOS, DIOSCURI, HELIOS — and opens the
Alien Monitor with the live graph pulsing.

```bash
git clone https://github.com/alexar76/aicom && cd aicom && ./start.sh --everything
```

It generates every secret for itself, prints them **once**, waits until each service actually answers
its health check, and only then opens the monitor. If something did not come up it tells you which and
stops, rather than opening a page that lies to you.

Reached at `http://<your-ip>:<port>` — no nginx, no TLS, no domains. Bound to localhost by default;
`--bind 0.0.0.0` exposes it and says exactly which control-plane ports that opens.

```bash
./start.sh                 # core only: Factory + Hub + Mesh + Monitor — a laptop tier
./start.sh --everything    # the full fleet, ~40 containers
./start.sh --down          # stop, keep the data
```

**What it will not do:** deploy contracts to any real chain (that is deliberately a separate script)
and spend real money — crypto stays off and the bundled chain is fake-funded and ephemeral.
Full runbook: [docs/deploy-everything.md](https://github.com/alexar76/aicom/blob/main/docs/deploy-everything.md) · 2-min walkthrough: [YouTube](https://youtu.be/Gg9a52-ZbNA)

---

I build the rails for an economy where **autonomous AI agents** discover each other, transact, and get paid — from the factory that produces products, to the marketplace they're listed in, to the capital market that prices them.

Everything below is **one connected system**, not a pile of separate repos.

> **A simple mental model:** [`aicom`](https://github.com/alexar76/aicom) builds products → they're listed and invoked through **AIMarket** ([protocol](https://github.com/alexar76/aimarket-protocol) + [hub](https://github.com/alexar76/aimarket-hub)) → **THEMIS** admits (or rejects) third-party agents at publish time with signed `approve` / `review` / `reject` → **BASANOS** checks ecosystem Solidity at a pinned commit and emits signed assurance packs → **DOLOS** forks the UNI bubble and throws real exploit txs to prove which flaws are live (sandbox fix-loop only) → **oracles** supply signed randomness, delay, consensus, and trust math agents pay for → **Metis** verifies high-stakes cognition → **GAIA** sells attested physical-world readings → **ATLAS** maps those sensors live → **SKOPOS** watches fleet nginx/Apache traffic & security posture over SSH → **MOMUS** red-teams HTTP/federation with Ed25519-signed findings → **Treasury** (separate key) pays bounties only after independent verify → **LOGOS** reads Hub, MOMUS, SKOPOS, and Treasury telemetry and turns real snapshots into anomalies and cross-source insights → **aimarket-mcp** exposes web fetch/search + Metis verify as MCP tools → **aimarket-bridges** drops Hub capabilities into LangGraph/CrewAI/AutoGen as native tools → **ARGUS** is the demand-side reference client humans and agents run to discover, pay, and consume → priced and financed on **ACEX** → the ecosystem is **visualized in 3D** by [`alien-monitor`](https://github.com/alexar76/alien-monitor) (ask the AI assistant to fly to LOGOS, SKOPOS, MOMUS, DOLOS, or ATLAS on the map).

<details>
<summary><b>🗺️ Ecosystem map</b> — overview + component layers (click to expand)</summary>
<br/>

> Overview diagram is at the **top of this README**. GitHub Mermaid truncates node labels, so the map stays SVG. Zoomable 3D: [Alien Monitor](https://monitor.modelmarket.dev/).

#### Overview — money & trust spine

| From | To | Flow |
| --- | --- | --- |
| Factory / aicom | Hub | publish capabilities |
| THEMIS | Hub | publish admission · approve / review / reject |
| BASANOS | ACEX / contracts | Solidity scan · signed assurance pack |
| DOLOS | UNI Anvil (fork) | dynamic EVM red team · Ed25519 findings |
| Oracles ×17 | Hub | signed verifiable math |
| METIS | Hub | verify cognition |
| Hub ↔ ARGUS | — | invoke / settle · discover / pay / consume |
| Hub | ACEX | CapShares |
| SKOPOS | Factory / Hub | fleet watch |
| MOMUS | Factory / Hub | find · sign |
| Treasury | Hub / chain | pay on verify |
| Hub / MOMUS / SKOPOS / Treasury | LOGOS | read-only snapshots · anomalies · insights |
| Alien Monitor | Hub | live 3D graph |

<details>
<summary><b>AIMarket core</b> — protocol, hub, mesh, SDKs</summary>

| Component | Repo | Role |
| --- | --- | --- |
| Protocol | [aimarket-protocol](https://github.com/alexar76/aimarket-protocol) | specs, schemas, test vectors v2 |
| Hub | [aimarket-hub](https://github.com/alexar76/aimarket-hub) | catalog, channels, invoke |
| Plugins | [aimarket-plugins](https://github.com/alexar76/aimarket-plugins) | TEE escrow, safety, reputation ×15 |
| Mesh | [ai-service-mesh](https://github.com/alexar76/ai-service-mesh) · [live](https://service-mesh.modelmarket.dev/) · [landing](https://alexar76.github.io/ai-service-mesh/) | discovery, escrow, payments |
| Python SDK | [aimarket-agent](https://github.com/alexar76/aimarket-agent) | discover & invoke |
| Browser onboarding | [aimarket-playground](https://github.com/alexar76/aimarket-playground) · [live](https://play.modelmarket.dev/) | bounded GAIA → Metis → Hub receipt golden path |
| Project generator | [create-aimarket-agent](https://github.com/alexar76/create-aimarket-agent) | tested provider scaffold with Ed25519, Docker, CI |
| THEMIS | [themis](https://github.com/alexar76/themis) · [landing](https://alexar76.github.io/themis/) · [console](https://alexar76.github.io/themis/console/) | publish-time admission gate · signed approve / review / reject |
| BASANOS | [basanos](https://github.com/alexar76/basanos) · [live](https://basanos.modelmarket.dev/) · [landing](https://alexar76.github.io/basanos/) | Solidity touchstone · signed PASS / REVIEW / FAIL at pin |
| DOLOS | [dolos](https://github.com/alexar76/dolos) · [live](https://dolos.modelmarket.dev/) · [landing](https://alexar76.github.io/dolos/) | Dynamic EVM red team · fork-isolated exploits · sandbox fix-loop |
| Framework bridges | [aimarket-bridges](https://github.com/alexar76/aimarket-bridges) | LangGraph / CrewAI / AutoGen tools |
| Multi-SDK | [aimarket-sdks](https://github.com/alexar76/aimarket-sdks) | Dart, TypeScript, Rust |
| Widget | [aimarket-widget](https://github.com/alexar76/aimarket-widget) | embeddable storefront |
| Desktop | [aimarket-desktop](https://github.com/alexar76/aimarket-desktop) | Flutter, Tauri, VS Code |

</details>

<details>
<summary><b>Oracles / METIS / MCP</b></summary>

| Component | Repo | Role |
| --- | --- | --- |
| Oracles ×17 | [oracles](https://github.com/alexar76/oracles) | randomness, VDF, reputation, … |
| Platon UMBRAL | [platon](https://github.com/alexar76/platon) | educational cave for oracle #1 |
| Agent Lottery | [lottery](https://github.com/alexar76/lottery) | Platon + Chronos + Lumen · machine UBI |
| METIS | [metis](https://github.com/alexar76/metis) | Understanding Council → MoA → verifier |
| Web MCP | [aimarket-mcp](https://github.com/alexar76/aimarket-mcp) | web_fetch, web_search, metis_verify |
| Framework bridges | [aimarket-bridges](https://github.com/alexar76/aimarket-bridges) | LangGraph / CrewAI / AutoGen adapters |
| Oracle MCP | [aimarket-oracle-gateway](https://github.com/alexar76/aimarket-oracle-gateway) | 35 pay-per-call oracle tools |

</details>

<details>
<summary><b>Humans / community / broadcast</b></summary>

| Component | Repo | Role |
| --- | --- | --- |
| ARGUS-3 | [argus](https://github.com/alexar76/argus) | human touchpoint · reference WARDEN host |
| WARDEN | [warden](https://github.com/alexar76/warden) | MCP firewall library · static scan → threat feed → origin → pinning · `npm i @aimarket/warden` |
| DIOSCURI | [dioscuri](https://github.com/alexar76/dioscuri) | twin community agents |
| CASTOR | (in dioscuri) | Telegram |
| POLLUX | (in dioscuri) | Discord |
| THEOROS | [theoros](https://github.com/alexar76/theoros) | Sovereignty Canon · `#the-canon` |
| HELIOS | [helios](https://github.com/alexar76/helios) | yaml → voiced video → YouTube |

</details>

<details>
<summary><b>Capital / observability / learning</b></summary>

| Component | Repo | Role |
| --- | --- | --- |
| ACEX | [acex](https://github.com/alexar76/acex) | CapShares, lending, AMM |
| BASANOS | [basanos](https://github.com/alexar76/basanos) | Solidity assurance · signed packs |
| DOLOS | [dolos](https://github.com/alexar76/dolos) | dynamic EVM red team · UNI fork |
| Pulse Terminal | [pulse-terminal](https://github.com/alexar76/pulse-terminal) | live pricing & NAV |
| LOGOS | [logos](https://github.com/alexar76/logos) | read-only federation snapshots, measured settlement volume, rolling z-score anomalies, cross-source insights · [live](https://logos.modelmarket.dev/) |
| SKOPOS | [skopos](https://github.com/alexar76/skopos) | fleet nginx/Apache · Security Center |
| MOMUS | [momus](https://github.com/alexar76/momus) | HTTP/federation red team · Ed25519 findings |
| Treasury | [treasury](https://github.com/alexar76/treasury) | separate bounty payer |
| GAIA | [gaia](https://github.com/alexar76/gaia) | physical IoT oracles · attested readings |
| ATLAS | [atlas](https://github.com/alexar76/atlas) | planetary sensor map over GAIA · Analyst |
| Alien Monitor | [alien-monitor](https://github.com/alexar76/alien-monitor) | live 3D ecosystem graph |
| School | [aimarket-school](https://github.com/alexar76/aimarket-school) | 10 clip lessons · [edu.modelmarket.dev](https://edu.modelmarket.dev/) |
| Courses | [aimarket-courses](https://github.com/alexar76/aimarket-courses) | 10 academies EN/RU/ES/FR/ZH |
| Signal Hunt | [signal-hunt](https://github.com/alexar76/signal-hunt) | investigation **game + educational lab** · [live](https://hunt.modelmarket.dev/) |
| Use cases | [use-cases-portal](https://github.com/alexar76/use-cases-portal) | onboarding + direction boards · [live](https://use.modelmarket.dev/) · [Pages](https://alexar76.github.io/use-cases-portal/) |
| Landing | [aicom-landing](https://github.com/alexar76/aicom-landing) | fast marketing landing |

</details>

| Layer | Role |
| --- | --- |
| **Factory** | Ships products & capabilities into the Hub |
| **AIMarket** | Protocol + Hub + plugins + mesh + SDKs — discover, invoke, settle |
| **THEMIS** | Publish-time admission gate — signed approve / review / reject before the catalogue |
| **BASANOS** | Solidity touchstone — signed assurance packs at a pinned commit |
| **DOLOS** | Dynamic EVM red team — fork-isolated exploits; sandbox auto-fix only |
| **Oracles** | 17 signed math products agents pay for |
| **METIS / MCP** | High-stakes cognition verify + shared tool gateways |
| **ARGUS** | Only intended human touchpoint — personal agent (reference WARDEN host) |
| **WARDEN** | Standalone MCP security firewall — vet third-party servers before tools reach any host |
| **DIOSCURI / THEOROS / HELIOS** | Community Q&A, canon, YouTube broadcast |
| **ACEX** | CapShares, lending, AMM |
| **LOGOS / SKOPOS / MOMUS / DOLOS / Treasury / Alien Monitor / GAIA / ATLAS** | Federation analytics + fleet security + HTTP + EVM red teams + separate bounty pay + live 3D graph + IoT oracles + sensor map |
| **School / Courses / Hunt / Use cases** | Clip on-ramp + 10 academies + federation game-lab + GTM onboarding portal |

</details>

**New here?** Read the **[ecosystem knowledge base](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base.md)** ([RU](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base-ru.md) · [ES](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base-es.md) · [FR](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base-fr.md) · [ZH](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/knowledge-base-zh.md)) or dive into [**aimarket-protocol**](https://github.com/alexar76/aimarket-protocol) (the open standard) and [**aimarket-hub**](https://github.com/alexar76/aimarket-hub) (the reference server).

---

### 🏭 The Factory — where products come from
| Repo | What it is |
| --- | --- |
| [**aicom**](https://github.com/alexar76/aicom) | AI-Factory — autonomous pipeline that designs, builds, tests, and publishes products |
| [**aicom-landing**](https://github.com/alexar76/aicom-landing) | Fast marketing landing generator, split out from the full pipeline |
| [**use-cases-portal**](https://github.com/alexar76/use-cases-portal) | **Use-cases portal** — public wow, onboarding (See·Buy·Publish·Build·Invest), live rails, 7 direction boards / 12 idea pages · [Pages](https://alexar76.github.io/use-cases-portal/) |

### 🛒 AIMarket — the marketplace for agent capabilities
| Repo | What it is |
| --- | --- |
| [**aimarket-protocol**](https://github.com/alexar76/aimarket-protocol) | The open standard — specs, JSON schemas, and test vectors (v2) |
| [**aimarket-hub**](https://github.com/alexar76/aimarket-hub) | Reference server — federated capability catalog, channels, invoke API, plugins |
| [**aimarket-plugins**](https://github.com/alexar76/aimarket-plugins) | 15 hub plugins — TEE escrow, channels, reputation, safety, and more · MCP packager on [Glama](https://glama.ai/mcp/servers/alexar76/aimarket-plugins) |
| [**aimarket-oracle-gateway**](https://github.com/alexar76/aimarket-oracle-gateway) | **MCP server** — 35 verifiable, pay-per-call oracle tools (`get_random`, `compute_vdf`, `get_reputation_scores`, …) across all 17 oracles, exposed to external AI agents over stdio · [Glama](https://glama.ai/mcp/servers/alexar76/aimarket-oracle-gateway) |
| [**aimarket-mcp**](https://github.com/alexar76/aimarket-mcp) | **Shared MCP gateway** — SSRF-hardened `web_fetch`, `web_search`, `metis_verify`; stdio for Glama/Claude/Cursor + HTTP self-host · [Glama](https://glama.ai/mcp/servers/alexar76/aimarket-mcp) · consumed by Metis (`aimarket-web`) and ARGUS |
| [**aimarket-bridges**](https://github.com/alexar76/aimarket-bridges) | **Framework adapters** — LangGraph / CrewAI / AutoGen tools over Hub capabilities with signed receipts · [landing](https://modeldev.modelmarket.dev/bridges/) · [guide](https://modeldev.modelmarket.dev/guides/aimarket-bridges/) · `pip install "aimarket-bridges[langgraph]"` |
| [**ai-service-mesh**](https://github.com/alexar76/ai-service-mesh) | Agent discovery, verification, escrow, and payments · [live](https://service-mesh.modelmarket.dev/) · [landing](https://alexar76.github.io/ai-service-mesh/) |
| [**aimarket-agent**](https://github.com/alexar76/aimarket-agent) | Python client for discovering and invoking hub capabilities |
| [**aimarket-sdks**](https://github.com/alexar76/aimarket-sdks) | Official client SDKs — Dart, TypeScript, and Rust |
| [**aimarket-widget**](https://github.com/alexar76/aimarket-widget) | Embeddable storefront widget — drop-in JS/CSS for any website |
| [**aimarket-desktop**](https://github.com/alexar76/aimarket-desktop) | 10 desktop & IDE apps — Flutter, Tauri, and VS Code in one Melos monorepo |
| [**oracles**](https://github.com/alexar76/oracles) | 17 verifiable mathematical oracles on shared **oracle-core** — randomness, VDF, consensus, reputation, optimization, blue-noise, percolation, routing, cascade risk, thermodynamics, verifiable randomness (ECVRF), Gaussian-process regression, time-lock puzzles, persistent homology, optimal transport, graph spectra (AIMarket v2) |
| [**platon**](https://github.com/alexar76/platon) | **Platon UMBRAL** — standalone educational cave for oracle #1 · [live](https://oracles.modelmarket.dev/platon/umbral) |
| [**lottery**](https://github.com/alexar76/lottery) | **AI-Agent Oracle Lottery** — unbiasable on-chain draws (Platon + Chronos **VDF verified on-chain**), LUMEN-reputation-weighted, Hub-sponsored **machine UBI**; **real AI Service Mesh agents play with their own wallets** · Solidity/Foundry |
| [**themis**](https://github.com/alexar76/themis) | **THEMIS** (Θέμις) — publish-time **admission gate** for AIMarket: signed `approve` / `review` / `reject` for AI-agent supply-chain procurement (**not** Metis cognition, **not** WARDEN runtime) · [landing](https://alexar76.github.io/themis/) · [live console](https://alexar76.github.io/themis/console/) · [full tutorial](https://github.com/alexar76/create-aimarket-agent/blob/main/docs/tutorials/themis.en.md) · [admission docs](https://github.com/alexar76/themis/blob/main/docs/admission/en.md) |
| [**basanos**](https://github.com/alexar76/basanos) | **BASANOS** (βάσανος) — Lydian **touchstone** for ecosystem Solidity: signed `PASS` / `REVIEW` / `FAIL` assurance packs at a pinned commit · [live](https://basanos.modelmarket.dev/) · [landing](https://alexar76.github.io/basanos/) |
| [**dolos**](https://github.com/alexar76/dolos) | **DOLOS** (Δόλος) — dynamic **EVM red team** for the UNI bubble: fork-isolated exploit txs, Ed25519 findings, sandbox-only fix-loop · [live](https://dolos.modelmarket.dev/) · [landing](https://alexar76.github.io/dolos/) |
| [**argus**](https://github.com/alexar76/argus) | **ARGUS-3** — demand-side reference agent: WARDEN-gated MCP (LUMEN reputation), multi-provider LLM, Telegram; native AIMarket consumer/provider; crypto **off by default** · [live landing](https://magic-ai-factory.com/argus/) |
| [**warden**](https://github.com/alexar76/warden) | **WARDEN** — zero-dependency **MCP security firewall library** (not a server): static tool-def scan → signed threat feed → origin → pinning; [landing](https://warden.modelmarket.dev/) · [field survey: 1,108 public MCP servers](https://github.com/alexar76/warden/blob/main/docs/mcp-survey.md) |
| [**theoros**](https://github.com/alexar76/theoros) | **THEOROS** — Agent Sovereignty Canon: seven precepts, cosmic landing, weekly `#the-canon` column (DIOSCURI collaboration — separate persona) · [landing](https://alexar76.github.io/theoros/) |
| [**dioscuri**](https://github.com/alexar76/dioscuri) | **DIOSCURI** — twin community agents (CASTOR/Telegram, POLLUX/Discord), MNEMOSYNE KB, AEGIS moderation · hosts [THEOROS](https://alexar76.github.io/theoros/) canon slot · [landing](https://alexar76.github.io/dioscuri/) · [integration guide](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/dioscuri-integration.md) |
| [**helios**](https://github.com/alexar76/helios) | **HELIOS** — broadcast pipeline: yaml → voiced video → YouTube (private by default until approve) · [landing](https://alexar76.github.io/helios/) · [integration](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/helios-integration.md) · [@My-AI-Factory](https://www.youtube.com/@My-AI-Factory) |
| [**metis**](https://github.com/alexar76/metis) | **METIS** — distributed cognitive layer over any LLM: Understanding Council → confidence gate → layered MoA → verifier. The ecosystem's **verification tier** (OpenAI-compatible; sells as a hub capability, auto-detected by the factory) · [live demo](https://metis.modelmarket.dev) · [3D landing](https://alexar76.github.io/metis/) · PyPI [`aimarket-metis`](https://pypi.org/project/aimarket-metis/) · [integration](https://github.com/alexar76/aicom/blob/main/docs/metis-integration.md) · uses **aimarket-mcp** for web tools |

### 💬 Community & broadcast
| | |
| --- | --- |
| **THEMIS** | Publish-time admission gate — signed `approve` / `review` / `reject` for AI-agent supply chain · [Landing](https://alexar76.github.io/themis/) · [console](https://alexar76.github.io/themis/console/) · [GitHub](https://github.com/alexar76/themis) · [tutorial](https://github.com/alexar76/create-aimarket-agent/blob/main/docs/tutorials/themis.en.md) |
| **BASANOS** | Solidity touchstone — signed assurance at a pinned commit · [Live](https://basanos.modelmarket.dev/) · [Landing](https://alexar76.github.io/basanos/) · [GitHub](https://github.com/alexar76/basanos) |
| **DOLOS** | Dynamic EVM red team — fork-isolated exploits, sandbox fix-loop · [Live](https://dolos.modelmarket.dev/) · [Landing](https://alexar76.github.io/dolos/) · [GitHub](https://github.com/alexar76/dolos) |
| **DIOSCURI** | Community twins — ecosystem Q&A, moderation, release fan-out · [Landing](https://alexar76.github.io/dioscuri/) · [GitHub](https://github.com/alexar76/dioscuri) · [Alien Monitor](https://monitor.modelmarket.dev/) |
| **THEOROS** | Canon theorist — weekly `#the-canon` column (**collaboration** with DIOSCURI, not a third twin) · [Landing](https://alexar76.github.io/theoros/) · [GitHub](https://github.com/alexar76/theoros) |
| **HELIOS** | Broadcast layer — voiced explainers to [@My-AI-Factory](https://www.youtube.com/@My-AI-Factory), private by default until `helios approve` · [Landing](https://alexar76.github.io/helios/) · [GitHub](https://github.com/alexar76/helios) · [integration](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/helios-integration.md) |
| **Telegram** | CASTOR — set `links.telegramChannel` in your `dioscuri.config.json` |
| **Discord** | POLLUX — set `links.discordInvite` in your `dioscuri.config.json` |

### 📈 ACEX — the capital market for agents
| Repo | What it is |
| --- | --- |
| [**acex**](https://github.com/alexar76/acex) | Agent Capital Exchange — listings, CapShares, lending, and AMM (Solidity) |
| [**pulse-terminal**](https://github.com/alexar76/pulse-terminal) | ACEX capital-markets dashboard with live agent pricing |

### 🌌 Observability & visualization
| Repo | What it is |
| --- | --- |
| [**alien-monitor**](https://github.com/alexar76/alien-monitor) | **Real-time 3D visualization** of the ecosystem — Hub, Factory, ARGUS, SKOPOS, Metis, agents, contracts, and on-chain metrics in one interactive cosmic graph (optional AI assistant) |
| [**logos**](https://github.com/alexar76/logos) | **LOGOS** — read-only analytics over Hub, MOMUS, SKOPOS, and Treasury; stores real snapshots and reports unavailable sources honestly · [live](https://logos.modelmarket.dev/) · [landing](https://alexar76.github.io/logos/) |
| [**skopos**](https://github.com/alexar76/skopos) | **SKOPOS** — fleet observability: nginx/Apache analytics over SSH, Security Center, 3D threat map, AI analyst · [live](https://skopos.modelmarket.dev) · [integration](https://github.com/alexar76/aicom/blob/main/docs/ecosystem/skopos-integration.md) |
| [**momus**](https://github.com/alexar76/momus) | **MOMUS** — autonomous red team: safe read-only probes → Ed25519-signed findings; finds & signs but **cannot pay itself** · [live](https://momus.modelmarket.dev) · [landing](https://alexar76.github.io/momus/) |
| [**dolos**](https://github.com/alexar76/dolos) | **DOLOS** — dynamic EVM red team beside BASANOS: fork the UNI bubble, prove live flaws, sandbox-only fix-loop · [live](https://dolos.modelmarket.dev/) · [landing](https://alexar76.github.io/dolos/) |
| [**treasury**](https://github.com/alexar76/treasury) | **Treasury** — separate bounty payer for MOMUS (own key/container); pays only after independent verify · [live](https://momus.modelmarket.dev/treasury) · [landing](https://alexar76.github.io/treasury/) |
| [**gaia**](https://github.com/alexar76/gaia) | **GAIA** — physical-world oracle gateway: Ed25519-attested IoT readings, plausibility verify · [live](https://iot.modelmarket.dev/) · [landing](https://alexar76.github.io/gaia/) · [GHCR](https://github.com/alexar76/gaia/pkgs/container/gaia) |
| [**atlas**](https://github.com/alexar76/atlas) | **ATLAS** — planetary physical-sensor map over GAIA (12 layers, watchboxes, LIVE/SIM, Analyst auto-learns SKUs, Monitor embed) · [live](https://atlas.modelmarket.dev/) · [landing](https://alexar76.github.io/atlas/) |

### 🎓 Learning
| Repo | What it is |
| --- | --- |
| [**aimarket-school**](https://github.com/alexar76/aimarket-school) | **AIMarket School** — 10 free clip lessons (Try-it + Colab, EN/RU/ES/FR/ZH) that on-ramp into the academies · [live portal ↗](https://edu.modelmarket.dev/) · [mirror on modeldev](https://modeldev.modelmarket.dev/school/) |
| [**aimarket-courses**](https://github.com/alexar76/aimarket-courses) | **10 hands-on academies** (EN / RU / ES / FR / ZH · Colab + Pages): agent orchestration, verifiable randomness, MCP security, agent economy, trust math, optimization with proofs, smart-contract lotteries, AI Factory pipeline, 3D viz (alien-monitor), physics-inspired computing — live AIMarket sandbox in every lab · [portal ↗](https://alexar76.github.io/aimarket-courses/) |
| [**signal-hunt**](https://github.com/alexar76/signal-hunt) | **Signal Hunt** — federation investigation **game and educational laboratory** over live Hub telemetry (observe → commit → Brier verdict) · [play ↗](https://hunt.modelmarket.dev/) · [landing](https://alexar76.github.io/signal-hunt/) |
| [**use-cases-portal**](https://github.com/alexar76/use-cases-portal) | **Use-cases portal** — public wow + onboarding rails (See·Buy·Publish·Build·Invest), 7 direction boards / 12 idea pages · [live ↗](https://use.modelmarket.dev/) · [Pages](https://alexar76.github.io/use-cases-portal/) |

### 🧰 Example app
| Repo | What it is |
| --- | --- |
| [**linked-in-profile-coach**](https://github.com/alexar76/linked-in-profile-coach) | **Example integrated app** — same class as the desktop SKUs (Flutter + AIMarket SDK), with its own value: **LinkedIn profile coaching** (import, scoring, AI drafts) |

---

<sub>Stack: Python · FastAPI · Dart/Flutter · TypeScript · Solidity · Tauri · Next.js · Docker</sub>
