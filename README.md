# Syntropy — Holons

<div align="right"><a href="./README_ES.md">Español</a> | English</div>

> **Order out of chaos for the age of AI agents.**
>
> The nine holons of [SyntropyOS](https://github.com/SyntropyOS), one directory each.

Each capability is a **holon**: autonomous yet connected — a whole in its own scope and
part of the Syntropy ecosystem at the same time.

**This repository is the substrate, not the product.** It exists because nine
repositories that each contained one file cost more to maintain than they proved. The
directory layout is the thesis made visible: every capability is a separate piece with
its own problem, its own customer and its own place in the build order.

---

## Build criterion

> A holon **is not built because it is on a roadmap**. It is built when a diagnosis in a
> real organization finds the chaos this holon resolves.

This criterion replaces prioritizing by technical interest, and it is why the
priorities changed. A holon with no diagnosed chaos behind it is a guess.

---

## The holons

| Holon | Function | The chaos it resolves | Status |
|---|---|---|---|
| [**Cardinal**](./holons/cardinal/) · [ES](./holons/cardinal/README_ES.md) | Orientation | **Context**: what we know, when we learned it, and from whom | In build · 1st |
| [**Iris**](./holons/iris/) · [ES](./holons/iris/README_ES.md) | Vision | **Perception**: what is an image or paper nobody can query | In build · 2nd |
| [**Meta**](./holons/meta/) · [ES](./holons/meta/README_ES.md) | Metacognition | **Trust**: evidence that the AI told the truth | In build · 3rd |
| [**Execute**](./holons/execute/) · [ES](./holons/execute/README_ES.md) | Execution | **Execution**: the automation breaks and nobody repairs it | Defined |
| [**Sage**](./holons/sage/) · [ES](./holons/sage/README_ES.md) | Adaptation | **Adaptation**: neither the system nor the people adapt | Defined |
| [**Plan**](./holons/plan/) · [ES](./holons/plan/README_ES.md) | Planning | **Decomposition**: nobody breaks the work down | Defined |
| [**Orchestra**](./holons/orchestra/) · [ES](./holons/orchestra/README_ES.md) | Coordination | **Runtime**: without it, the holons do not know how to cooperate | Defined · once 2+ exist |
| [**Reverb**](./holons/reverb/) · [ES](./holons/reverb/README_ES.md) | Audio | Out of initial scope | Deferred |
| [**Reason**](./holons/reason/) · [ES](./holons/reason/README_ES.md) | Reasoning | Out of initial scope | Deferred |

**Defined** means the design and activation criteria are documented; it does not mean it
ships. Only the substrate (VantaDB) is in production today.

**Cardinal** comes first because the others depend on it: without verifiable context there
is nothing to perceive and nothing to verify. **Meta** moved from ninth to third because
it is the differentiator — the competition sells capability, this sells verifiability.

**Plan** appears after Meta because its output is meant to be verifiable, and
verification is what Meta provides. It is not an independent capability.

**Sage** is adaptation in both halves: the machine learns from corrections, and the
people change how they work. Enterprise AI fails on adoption more often than on
accuracy, and no other holon covers that.

### The substrate

| Component | What it is | Where |
|---|---|---|
| **VantaDB** | Memory with ACID, MVCC, WAL and HNSW/IVF/SCANN indexes | [`ness-e/Vantadb`](https://github.com/ness-e/Vantadb) · v0.7.0 in production |

VantaDB is the one holon already built. It lives in its own repository because it is a
released library with an independent version cycle. Everything in *this* repository is
what is missing.

---

## Correspondence with the standard agent architecture

The holons are not an invention. They map onto the canonical decomposition of an agent
architecture:

| Standard component | Holon |
|---|---|
| Perception & input processing | Iris |
| Reasoning engines | Plan |
| Memory systems | VantaDB |
| **Episodic memory** | **Cardinal** |
| Tool execution | Execute |
| Orchestration & state management | Orchestra |
| Knowledge retrieval & augmentation | Cardinal |
| Observability, audit and governance | Meta |
| Feedback loops / adaptation | Sage |

**Episodic memory** is identified by the industry as a capability that is missing and that
production frameworks treat only superficially. That is Cardinal, and it is a real gap.

---

## The four surfaces of every holon

| Surface | For whom | Form |
|---|---|---|
| Developer | Whoever builds on it | API, SDK, MCP server, CLI |
| Agent | An AI system | Invocable MCP tools |
| Human | Non-technical person | Interface, upload, correction |
| Enterprise | Has to answer to someone | Governance panel, audit, SLA, isolation |

Hard rule: if a capability only exists inside a human interface, it is consultancy
disguised as software. Everything done for the client has to exist as an API.

---

## Build order

```
VantaDB  (substrate, in production)
   └─► 1. Cardinal   context       ┐
   └─► 2. Iris       perception    ├─ without Cardinal there is nothing to verify
   └─► 3. Meta       trust         ┘
   └─► 4. Execute    execution     requires prior trust
   └─► 5. Sage       adaptation   requires trustworthy context and Iris
   └─► 6. Plan       decomposition requires something to verify the steps against
          Orchestra   runtime       once two holons are alive
```

No dates. The order comes out of the diagnosis, not out of a calendar.

`Reverb` and `Reason` are deferred with written reactivation conditions inside their own
READMEs. Deferral is not deletion: the condition that would bring each one back is on
record.

---

## Languages

Every document in this repository exists in English as the primary version, with Spanish
as an option:

```
README.md                        English  ← primary
README_ES.md                     Español
holons/<name>/README.md          English
holons/<name>/README_ES.md       Español
```

The same convention applies across the organization: `MANIFESTO.md`, `ROADMAP.md`,
`CONTRIBUTING.md` and the rest are English, with a `_ES.md` counterpart.

---

## Where the definitions live

This repository contains **what** we build. The **why** and the **for whom** live elsewhere:

| Repository | Visibility | Contents |
|---|---|---|
| [`SyntropyOS/.github`](https://github.com/SyntropyOS/.github) | public | Organization profile, manifesto, roadmap, governance |
| `strategy` | **private** | Master definition, market evidence, business model, competitive analysis |

The split is deliberate. Mixing "this is what we believe" with "this is what we know
about the market" degrades both.

---

## License

Apache 2.0 — see [LICENSE](./LICENSE).

---

> **History.** This monorepo replaced nine per-holon repositories, `syntropy-<holon>`,
> deleted on 29 September 2026. Each was merged with `git subtree`, so all 27 original
> commits survive here with their original authors and dates. Their history lives inside the
> monorepo.
