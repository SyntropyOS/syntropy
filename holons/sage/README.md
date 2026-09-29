# Syntropy Sage

> **Adaptation** - Holon of [SyntropyOS](https://github.com/SyntropyOS)

<div align="right"><a href="./README_ES.md">Español</a> | English</div>

**Status: Defined** - Position in the chain: **5 of 6**

---

## The chaos it resolves

**Adaptation**: nobody adapts. The system repeats what it was already corrected on, and the people repeat what they were already shown.

This holon exists because that chaos gets diagnosed in real organizations. If a
diagnosis does not find it, it does not get built.

## Theory

Adaptation is **per organization**, not global. A model tuned for one company is useless for another. And the half that gets ignored: the people do not adapt either. Systems reach production or they do not, and the deciding factor is usually whether someone changed how they work, not whether the model got smarter.

## What it produces

Capture of corrections as first-party training data, plus the human half: who adopted what, who overrode it, who escalated, and why. Local adaptation per domain and per customer, for the machine and for the workflow. Isolation: one customer's learning does not contaminate another's.

## Validation signal

> Who used this last week, and what did they do with the answer? If the answer is nobody, the bottleneck is adoption and not accuracy.

### Why adaptation includes people

Enterprise AI fails more often on adoption than on accuracy. The measured causes are organizational: no agreed definition of success, no change management, and no named production owner. Three of the five things the projects that reach production do before writing code are organizational, and none of the three is about model quality.

So this holon carries both halves on purpose. The machine half is ordinary fine-tuning territory. The human half — measuring behaviour, not accuracy, and feeding corrections back into the workflow — is what the industry skips, and it is where the money is.

### Why it comes fifth, on purpose

Learning on untrusted context **amplifies** the error instead of correcting it. Both halves need Cardinal and Iris working first: you cannot adapt on a foundation nobody can trace.


## Dependencies

Cardinal, Iris and Meta.

## Surfaces

| Surface | For whom | Form |
|---|---|---|
| Developer | Whoever builds on it | API, SDK, MCP server, CLI |
| Agent | An AI system | Invocable MCP tools |
| Human | Non-technical person | Interface, upload, correction |
| Enterprise | Has to answer to someone | Governance panel, audit, SLA, isolation |

Hard rule: if a capability only exists inside a human interface, it is consultancy disguised as
software. Everything done for the client has to exist as an API.

## Reference price

To be defined by scope

## Build criterion

> A holon **is not built because it is on a roadmap**. It is built when a diagnosis in a real
> organization finds the chaos this holon resolves.

See the [SyntropyOS ROADMAP](https://github.com/SyntropyOS/.github/blob/main/ROADMAP.md) for the
full order and the reactivation conditions.

## License

Apache 2.0 - see [LICENSE](./LICENSE).