# Roadmap — Cardinal

> Contexto verificable. Criterio: se construye solo si un diagnóstico encuentra el caos.

## Fases

| Fase | Qué | Exit |
|---|---|---|
| Investigación | Stack + benchmarks + precios (ver strategy/11) | URLs primarias archivadas |
| Análisis | Caos x3 en 5 mapas | Señal medible definida |
| Desarrollo | API+MCP+log | Criterio aceptación verificable |
| Implementación | Piloto 1 empresa | Mapa + cobro |

Ver ROADMAP global: https://github.com/SyntropyOS/.github/blob/main/ROADMAP.md

---

## Producto (software)

Memoria episodica gobernada sobre VantaDB.

## Metodologia (como se entrega)

MCP server + API + CLI de ingesta/consulta con posicion-tiempo-procedencia y budget de tokens por respuesta.

## Proyecto entrada (1k-4k)

Piloto 100: 1 fuente + 50 hechos con cita. Holon 1k-4k: Cardinal vivo con log.

## Pendiente investigar internet

Zep/Graphiti temporal vs Mem0; LoCoMo/LongMemEval; Zep Cloud Flex 125.

## Storage

Usa VantaDB como implementación de referencia. Posee la semántica episódica (posición, tiempo, procedencia) y el budget de tokens — sobrevive si cambia el backend.
