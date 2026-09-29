# Syntropy — Holones

> **Orden desde el caos para la era de los agentes de IA.**
>
> Monorepo de los holones de [SyntropyOS](https://github.com/SyntropyOS).

Cada capacidad es un **holón**: autónomo pero conectado — un todo en su ámbito y
parte de un todo mayor (marco de Koestler, 1967).

**La arquitectura de este repositorio es la tesis, no una decisión de
organización.** Un directorio por holón hace visible que cada capacidad es una
pieza separada con su propio problema, su propio cliente y su propio orden de
construcción.

---

## El criterio de construcción

> Un holón **no se construye porque esté en un roadmap**. Se construye cuando un
> diagnóstico en una organización real encuentra el problema que resuelve.

Este criterio sustituye a la priorización por interés técnico, y es la razón de
que las prioridades hayan cambiado.

---

## Los holones

| Holón | Función | El problema que resuelve | Estado |
|---|---|---|---|
| [**Cardinal**](./holons/cardinal/) | Orientación | **Contexto**: qué sabemos, cuándo lo supimos y de quién | En construcción · 1º |
| [**Iris**](./holons/iris/) | Visión | **Percepción**: lo que es imagen o papel y nadie puede consultar | En construcción · 2º |
| [**Meta**](./holons/meta/) | Metacognición | **Confianza**: probar que la IA dijo la verdad, con evidencia | En construcción · 3º |
| [**Execute**](./holons/execute/) | Ejecución | **Ejecución**: la automatización se rompe y nadie la repara | Definido |
| [**Sage**](./holons/sage/) | Aprendizaje | **Aprendizaje**: el sistema repite lo que ya se le corrigió | Definido |
| [**Plan**](./holons/plan/) | Planificación | Complementario: descomponer el trabajo en pasos verificables | Definido |
| [**Orchestra**](./holons/orchestra/) | Coordinación | Runtime que hace cooperar a los demás holones | Definido · soporte |
| [**Reverb**](./holons/reverb/) | Audio | Fuera del alcance inicial | Aplazado |
| [**Reason**](./holons/reason/) | Razonamiento | Fuera del alcance inicial | Aplazado |

**Definido** significa diseño documentado y criterio de activación escritos; no
significa que esté construido.

**Cardinal** es el primero porque es prerrequisito de los demás: sin contexto
verificable no hay nada que perceptionar ni que verificar. **Meta** subió de
novena a tercera porque es el diferenciador: la competencia vende capacidad,
esto vende verificabilidad.

### El sustrato

| Componente | Qué es | Dónde |
|---|---|---|
| **VantaDB** | Memoria con ACID, MVCC, WAL e índices HNSW/IVF/SCANN | [`ness-e/Vantadb`](https://github.com/ness-e/Vantadb) · v0.5.0 en producción |

VantaDB es el holón construido. Este repositorio contiene los que faltan.

---

## Correspondencia con la arquitectura de la industria

Los holones no son una invención. Corresponden a la descomposición canónica de
una arquitectura de agentes:

| Componente estándar | Holón |
|---|---|
| Perception & input processing | Iris |
| Reasoning engines | Plan |
| Memory systems | VantaDB |
| **Episodic memory** | **Cardinal** |
| Tool execution | Execute |
| Orchestration & state management | Orchestra |
| Knowledge retrieval & augmentation | Cardinal |
| Observability, audit y governance | Meta |
| Feedback loops / adaptation | Sage |

La **memoria episódica** es identificada por la industria como una capacidad que
falta y que los frameworks de producción tratan de forma básica. Eso es
Cardinal, y es un hueco real.

---

## Superficies de cada holón

| Superficie | Para quién | Forma |
|---|---|---|
| Desarrollador | Quien construye | API, SDK, servidor MCP, CLI |
| Agente | Sistema de IA | Herramientas MCP invocables |
| Humana | Persona no técnica | Interfaz, carga, corrección |
| Empresa | Tiene que responder ante alguien | Panel de gobierno, auditoría, SLA |

Regla dura: si una capacidad solo existe dentro de una interfaz humana, es
consultoría disfrazada de software. Todo lo que se le hace al cliente tiene que
existir como API.

---

## Dónde está la definición

Este repositorio contiene **qué** construimos. El **por qué** y el **para quién**
viven en repositorios separados:

| Repositorio | Contenido |
|---|---|
| [`SyntropyOS/strategy`](https://github.com/SyntropyOS/strategy) · privado | Definición maestra, evidencia de mercado, modelo de negocio, método |
| [`SyntropyOS/.github`](https://github.com/SyntropyOS/.github) · público | Manifiesto, roadmap, perfil de la organización, gobernanza |

---

## Orden de construcción

```
VantaDB  (sustrato, en producción)
   └─► 1. Cardinal   contexto     ┐
   └─► 2. Iris       percepción   ├─ sin Cardinal no hay nada que verificar
   └─► 3. Meta       confianza    ┘
   └─► 4. Execute    ejecución     requiere confianza previa
   └─► 5. Sage       aprendizaje   requiere contexto confiable
   └─► 6. Plan       planificación
          Orchestra   runtime      cuando existan 2 holones vivos
```

No hay fechas. El orden sale del diagnóstico, no de un calendario.

---

## Licencia

Apache 2.0 — ver [LICENSE](./LICENSE).

> Este repositorio sustituye a los nueve repositorios individuales
> `syntropy-<holon>`, archivados el 28 de septiembre de 2026 con su historial
> preservado aquí.
