# Syntropy Execute

<div align="right"><a href="./README.md">English</a> | Español</div>
> **Ejecución** — Holon de [SyntropyOS](https://github.com/SyntropyOS)

**Estado: Definido** · Posición en la cadena: **4 de 6**

---

## El caos que resuelve

**Ejecución**: la automatización se rompe y nadie sabe por qué ni la repara.

Este holon existe porque ese caos se diagnostica en organizaciones reales. Si un
diagnóstico no lo encuentra, no se construye.

## Teoría

Automatización sin observabilidad es un pasivo, no un activo. Un sistema que falla en silencio es peor que un sistema que no existe.

## Qué produce

Capa de ejecución de acciones y herramientas. Registro completo de cada acción: quién, cuándo, con qué entrada y salida. Reproducción y reversión. Alertas de fallo con causa.

## Señal de validación

> ¿Cuánto tardan en enterarse de una automatización rota, y cuánto en repararla?

### Relación con MCP

La ejecución de herramientas en el mundo de agentes es MCP. Execute no compite con MCP: lo consume con la capa de auditoría que MCP no trae.

## Dependencias

Meta. Viene cuando ya hay confianza.

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

USD 15.000 – 25.000 por implementación

## Criterio de construcción

> Un holon **no se construye porque esté en un roadmap**. Se construye cuando un
> diagnóstico en una organización real encuentra el caos que este holon resuelve.

Ver el [ROADMAP de SyntropyOS](https://github.com/SyntropyOS/.github/blob/main/ROADMAP_ES.md)
para el orden completo y las condiciones de reactivación.

## Licencia

Apache 2.0 — ver [LICENSE](./LICENSE).
