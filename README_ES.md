# Syntropy — Holones

<div align="right"><a href="./README.md">English</a> | Español</div>

> **Orden desde el caos para la era de los agentes de IA.**
>
> Los nueve holones de [SyntropyOS](https://github.com/SyntropyOS), un directorio cada uno.

Cada capacidad es un **holón**: autónomo pero conectado — un todo en su ámbito y parte
del ecosistema Syntropy al mismo tiempo.

**Este repositorio es el sustrato, no el producto.** Existe porque nueve repositorios que
cada uno contenían un solo archivo costaban más de mantener de lo que demostraban. El
directorio es la tesis hecha visible: cada capacidad es una pieza aparte con su propio
problema, su propio cliente y su propio lugar en el orden de construcción.

---

## Criterio de construcción

> Un holón **no se construye porque esté en un roadmap**. Se construye cuando un
> diagnóstico en una organización real encuentra el caos que este holón resuelve.

Este criterio sustituye a la priorización por interés técnico, y es la razón de que las
prioridades hayan cambiado. Un holón sin caos diagnosticado detrás es una suposición.

---

## Los holones

| Holón | Función | El caos que resuelve | Estado |
|---|---|---|---|
| [**Cardinal**](./holons/cardinal/README_ES.md) · [EN](./holons/cardinal/) | Orientación | **Contexto**: qué sabemos, cuándo lo supimos y de quién | En construcción · 1º |
| [**Iris**](./holons/iris/README_ES.md) · [EN](./holons/iris/) | Visión | **Percepción**: lo que es imagen o papel y nadie puede consultar | En construcción · 2º |
| [**Meta**](./holons/meta/README_ES.md) · [EN](./holons/meta/) | Metacognición | **Confianza**: prueba de que la IA dijo la verdad | En construcción · 3º |
| [**Execute**](./holons/execute/README_ES.md) · [EN](./holons/execute/) | Ejecución | **Ejecución**: la automatización se rompe y nadie la repara | Definido |
| [**Sage**](./holons/sage/README_ES.md) · [EN](./holons/sage/) | Adaptación | **Adaptación**: ni el sistema ni las personas se adaptan | Definido |
| [**Plan**](./holons/plan/README_ES.md) · [EN](./holons/plan/) | Planificación | **Descomposición**: nadie descompone el trabajo | Definido |
| [**Orchestra**](./holons/orchestra/README_ES.md) · [EN](./holons/orchestra/) | Coordinación | **Runtime**: sin él, los holones no saben cooperar | Definido · cuando existan 2+ |
| [**Reverb**](./holons/reverb/README_ES.md) · [EN](./holons/reverb/) | Audio | Fuera del alcance inicial | Aplazado |
| [**Reason**](./holons/reason/README_ES.md) · [EN](./holons/reason/) | Razonamiento | Fuera del alcance inicial | Aplazado |

**Definido** significa que el diseño y los criterios de activación están documentados. No
significa que esté en producción. Hoy solo un holón está en producción.

**Cardinal** va primero porque los demás dependen de él: sin contexto verificable no hay
nada que perceptionar ni que verificar. **Meta** subió de novena a tercera porque es el
diferenciador — la competencia vende capacidad, esto vende verificabilidad.

**Plan** aparece después de Meta porque su salida debe ser verificable, y la verificación
es lo que aporta Meta. No es una capacidad independiente.

**Sage** es adaptación en las dos mitades: la máquina aprende de las correcciones, y las
personas cambian cómo trabajan. La IA empresarial falla más por adopción que por
precisión, y ningún otro holón cubre eso.

### El sustrato

| Componente | Qué es | Dónde |
|---|---|---|
| **VantaDB** | Memoria con ACID, MVCC, WAL e índices HNSW/IVF/SCANN | [`ness-e/Vantadb`](https://github.com/ness-e/Vantadb) · v0.5.0 en producción |

VantaDB es el único holón ya construido. Vive en su propio repositorio porque es una
librería publicada con un ciclo de versión independiente. Todo lo que hay en *este*
repositorio es lo que falta.

---

## Correspondencia con la arquitectura estándar de agentes

Los holones no son una invención. Corresponden a la descomposición canónica de una
arquitectura de agentes:

| Componente estándar | Holón |
|---|---|
| Percepción y procesamiento de entrada | Iris |
| Motores de razonamiento | Plan |
| Sistemas de memoria | VantaDB |
| **Memoria episódica** | **Cardinal** |
| Ejecución de herramientas | Execute |
| Orquestación y gestión de estado | Orchestra |
| Recuperación y ampliación del conocimiento | Cardinal |
| Observabilidad, auditoría y gobierno | Meta |
| Bucles de retroalimentación / adaptación | Sage |

La **memoria episódica** es identificada por la industria como una capacidad que falta y
que los frameworks de producción tratan de forma superficial. Eso es Cardinal, y es un
hueco real.

---

## Las cuatro superficies de cada holón

| Superficie | Para quién | Forma |
|---|---|---|
| Desarrollador | Quien construye | API, SDK, servidor MCP, CLI |
| Agente | Sistema de IA | Herramientas MCP invocables |
| Humana | Persona no técnica | Interfaz, carga, corrección |
| Empresa | Tiene que responder ante alguien | Panel de gobierno, auditoría, SLA, aislamiento |

Regla dura: si una capacidad solo existe dentro de una interfaz humana, es consultoría
disfrazada de software. Todo lo que se le hace al cliente tiene que existir como API.

---

## Orden de construcción

```
VantaDB  (sustrato, en producción)
   └─► 1. Cardinal   contexto       ┐
   └─► 2. Iris       percepción      ├─ sin Cardinal no hay nada que verificar
   └─► 3. Meta       confianza       ┘
   └─► 4. Execute    ejecución       requiere confianza previa
   └─► 5. Sage       adaptación      requiere contexto confiable e Iris
   └─► 6. Plan       descomposición  requiere contra qué verificar los pasos
          Orchestra   runtime        cuando existan dos holones vivos
```

No hay fechas. El orden sale del diagnóstico, no de un calendario.

`Reverb` y `Reason` están aplazados con condiciones de reactivación escritas dentro de sus
propios README. Aplazar no es borrar: la condición que los traería de vuelta está en
registro.

---

## Idiomas

Cada documento de este repositorio existe en inglés como versión principal, con español
como opción:

```
README.md                        English  ← principal
README_ES.md                     Español
holons/<nombre>/README.md        English
holons/<nombre>/README_ES.md     Español
```

La misma convención se aplica en toda la organización: `MANIFESTO.md`, `ROADMAP.md`,
`CONTRIBUTING.md` y el resto son inglés, con su contraparte `_ES.md`.

---

## Dónde vive la definición

Este repositorio contiene **qué** construimos. El **por qué** y el **para quién** viven
en otros sitios:

| Repositorio | Visibilidad | Contenido |
|---|---|---|
| [`SyntropyOS/.github`](https://github.com/SyntropyOS/.github) | público | Perfil de la organización, manifiesto, roadmap, gobernanza |
| `strategy` | **privado** | Definición maestra, evidencia de mercado, modelo de negocio, análisis competitivo |

La separación es deliberada. Mezclar «esto es lo que creemos» con «esto es lo que sabemos
del mercado» degrada ambas cosas.

---

## Licencia

Apache 2.0 — ver [LICENSE](./LICENSE).

---

> **Historial.** Este monorepo sustituyó a los nueve repositorios por holón
> `syntropy-<holon>`, archivados el 28 de septiembre de 2026. Cada uno se integró con
> `git subtree`, así que los 27 commits originales sobreviven aquí con sus autores y
> fechas. Los repositorios archivados siguen siendo legibles y dicen a dónde fue su
> contenido.
