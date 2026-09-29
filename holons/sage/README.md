# Syntropy Sage

> **Aprendizaje** — Holon de [SyntropyOS](https://github.com/SyntropyOS)

**Estado: Definido** · Posición en la cadena: **5 de 6**

---

## El caos que resuelve

**Aprendizaje**: el sistema no aprende de sus propias correcciones. Se re-enseña todo cada vez.

Este holon existe porque ese caos se diagnostica en organizaciones reales. Si un
diagnóstico no lo encuentra, no se construye.

## Teoría

La adaptación útil es **por organización**, no global. Un modelo afinado para una empresa no sirve para otra. El aprendizaje que importa se queda dentro de la organización y no se va a un proveedor externo.

## Qué produce

Captura de correcciones como datos de entrenamiento propios. Adaptación local por dominio y por cliente. Aislamiento: el aprendizaje de un cliente no contamina a otro.

## Señal de validación

> ¿Cuántas veces hay que re-enseñar lo mismo porque el sistema olvidó una corrección anterior?

Esta es la pregunta que se le hace a un cliente potencial para saber si necesita este
holon. Si la respuesta es «no hay problema», no hay venta. Y eso es correcto.

### Por qué va quinto

A propósito. Aprender sobre contexto no confiable **amplifica** el error en lugar de corregirlo. Necesita a Cardinal e Iris funcionando primero.

## Dependencias

Cardinal e Iris.

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

Por definir según alcance

## Criterio de construcción

> Un holon **no se construye porque esté en un roadmap**. Se construye cuando un
> diagnóstico en una organización real encuentra el caos que este holon resuelve.

Ver el [ROADMAP de SyntropyOS](https://github.com/SyntropyOS/.github/blob/main/ROADMAP_ES.md)
para el orden completo y las condiciones de reactivación.

## Licencia

Apache 2.0 — ver [LICENSE](./LICENSE).
