# Syntropy Sage

<div align="right"><a href="./README.md">English</a> | Español</div>
> **Adaptación** — Holon de [SyntropyOS](https://github.com/SyntropyOS)

**Estado: Definido** · Posición en la cadena: **5 de 6**

---

## El caos que resuelve

**Adaptación**: nadie se adapta. El sistema repite lo que ya se le corrigió, y las personas repiten lo que ya les mostraron.

Este holon existe porque ese caos se diagnostica en organizaciones reales. Si un
diagnóstico no lo encuentra, no se construye.

## Teoría

La adaptación es **por organización**, no global. Un modelo afinado para una empresa no sirve para otra. Y la mitad que todos ignoran: las personas tampoco se adaptan. Los sistemas llegan a producción o no llegan, y lo que suele decidirlo no es si el modelo se puso más inteligente, sino si alguien cambió cómo trabaja.

## Qué produce

Captura de correcciones como datos de entrenamiento propios, más la mitad humana: quién adoptó qué, quién sobrescribió, quién escaló y por qué. Adaptación local por dominio y por cliente, para la máquina y para el flujo de trabajo. Aislamiento: el aprendizaje de un cliente no contamina a otro.

## Señal de validación

> ¿Quién usó esto la semana pasada, y qué hizo con la respuesta? Si la respuesta es nadie, el cuello de botella es la adopción y no la precisión.

### Por qué la adaptación incluye a las personas

La IA empresarial falla más por adopción que por precisión. Las causas medidas son
organizacionales: no hay definición de éxito acordada, no hay gestión del cambio, y no hay
un responsable de producción nombrado. Tres de las cinco cosas que hacen los proyectos que
sí llegan a producción —antes de escribir código— son organizacionales, y ninguna de las
tres es sobre calidad del modelo.

Por eso este holón carga las dos mitades a propósito. La mitad de máquina es territorio
común de ajuste fino. La mitad humana —medir comportamiento en vez de precisión, y
devolver las correcciones al flujo de trabajo— es lo que la industria se salta, y es donde
está el dinero.

### Por qué va quinto

A propósito. Aprender sobre contexto no confiable **amplifica** el error en lugar de corregirlo. Las dos mitades necesitan a Cardinal e Iris funcionando primero: no se puede adaptar sobre una base que nadie puede rastrear.

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
