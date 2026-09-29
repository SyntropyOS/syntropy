# Syntropy Execute

> **Execution** - Holon of [SyntropyOS](https://github.com/SyntropyOS)

<div align="right"><a href="./README_ES.md">Español</a> | English</div>

**Status: Defined** - Position in the chain: **4 of 6**

---

## The chaos it resolves

**Execution**: the automation breaks and nobody knows why, and nobody repairs it.

This holon exists because that chaos gets diagnosed in real organizations. If a
diagnosis does not find it, it does not get built.

## Theory

Automation without observability is a liability, not an asset. A system that fails silently is worse than a system that does not exist.

## What it produces

Execution layer for actions and tools. Full log of every action: who, when, with what input and output. Reproduction and rollback. Failure alerts with cause.

## Validation signal

> How long does it take to find out an automation broke, and how long to repair it?

### Relationship to MCP

Tool execution in the agent world is MCP. Execute does not compete with MCP: it consumes it and adds the audit layer MCP does not bring.


## Dependencies

Meta. It arrives once there is trust.

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

USD 15,000 - 25,000 per implementation

## Build criterion

> A holon **is not built because it is on a roadmap**. It is built when a diagnosis in a real
> organization finds the chaos this holon resolves.

See the [SyntropyOS ROADMAP](https://github.com/SyntropyOS/.github/blob/main/ROADMAP.md) for the
full order and the reactivation conditions.

## License

Apache 2.0 - see [LICENSE](./LICENSE).