# Syntropy Cardinal

<div align="right"><a href="./README.md">English</a> | Español</div>
> **Orientación** — Holon de [SyntropyOS](https://github.com/SyntropyOS)

**Estado: En construcción** · Posición en la cadena: **1 de 6**

---

## El caos que resuelve

**Contexto**: la organización no sabe qué sabe, ni cuándo lo supo, ni de quién lo supo.

Este holon existe porque ese caos se diagnostica en organizaciones reales. Si un
diagnóstico no lo encuentra, no se construye.

## Teoría

Todo hecho tiene tres atributos que lo hacen verificable: **posición** (dónde vive), **tiempo** (cuándo era cierto) y **procedencia** (quién lo afirmó). Sin los tres, la información se puede leer pero no se puede confiar. Cardinal convierte datos en contexto consultable.

## Qué produce

Índice gobernado del conocimiento organizacional con metadatos espacio-temporales. Responde *cuándo supimos esto* y *de dónde salió*. Es la base sobre la que escriben y leen los demás holones.

## Señal de validación

> ¿Cuánto tarda la organización en responder con fuente y fecha cuando la dirección hace una pregunta?

### Las tres funciones de la memoria, y cuál es esta

La taxonomía canónica de memoria agéntica la parte en tres, y Cardinal cubre dos:

| Función | Qué guarda | Cardinal |
|---|---|---|
| Factual | Conocimiento | **Formación** y **Recuperación** |
| Experiencial | Perspectivas y habilidades | No aquí — eso es Sage |
| De trabajo | Qué entra en el contexto activo | **Ver abajo** |

### La memoria de trabajo es parte de este holón

La memoria de trabajo no es otra base de datos. Es la decisión de qué entra en la ventana
de contexto en cada llamada, y es donde los sistemas en producción se rompen en silencio:
el contexto crece con cada transición entre agentes hasta que la calidad se degrada o la
factura de tokens se dispara.

Por eso la memoria de trabajo pertenece a Cardinal como restricción de recuperación: cada
respuesta trae un presupuesto de tokens, y lo que no se gana un lugar dentro de ese
presupuesto se queda fuera. Recuperación bajo presupuesto, no recuperación de todo. Es un
requisito de Cardinal, no un componente aparte.

## Dependencias

Ninguna. Es el primero.

## Superficies

| Superficie | Para quién | Forma |
|---|---|---|
| Desarrollador | Quien construye | API, SDK, servidor MCP, CLI |
| Agente | Sistema de IA | Herramientas MCP invocables |
| Humana | Persona no técnica | Interfaz, carga, corrección |
| Empresa | Tiene que responder ante alguien | Panel de gobierno, auditoría, SLA, aislamiento |

Regla dura: si una capacidad solo existe dentro de una interfaz humana, es
consultoría disfrazada de software. Todo lo que se le hace al cliente tiene que existir
como API.

## Precio de referencia

USD 8.000 – 15.000 por implementación

## Criterio de construcción

> Un holon **no se construye porque esté en un roadmap**. Se construye cuando un
> diagnóstico en una organización real encuentra el caos que este holon resuelve.

Ver el [ROADMAP de SyntropyOS](https://github.com/SyntropyOS/.github/blob/main/ROADMAP_ES.md)
para el orden completo y las condiciones de reactivación.

## Licencia

Apache 2.0 — ver [LICENSE](./LICENSE).
