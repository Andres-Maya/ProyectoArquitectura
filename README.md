# Dimensionamiento de Memos — Sustentación

Diapositivas del proyecto de Arquitectura del Computador: ¿en qué máquina debería correr Memos 0.31,
y con qué datos lo sostenemos?

Autores: Andrés Camilo Maya Rosero · Camilo Andrés Castro Acosta — noviembre de 2026.

- `index.html`: las 5 diapositivas de la sustentación (un solo archivo, sin dependencias externas).
  Controles: ← → para avanzar, **N** notas del expositor, **F** pantalla completa.

| # | Diapositiva | Idea |
|---|---|---|
| 1 | Portada | La pregunta y la respuesta: espera por CPU → AWS t3.small |
| 2 | Cómo medimos | k6, codo de 15 req/s, sostenida de 10 req/s × 10 min × 3 |
| 3 | Dónde espera | PSI de CPU 6,4 % vs. 2,6 % de disco, y su causa en la arquitectura |
| 4 | Tres opciones | Portátil, t3.small y contenedor limitado contra la misma demanda |
| 5 | ×10 y recomendación | Fallan login y escrituras; t3.small + contenedor de 1 núcleo / 512 MiB |

La versión anterior de 13 diapositivas queda en el historial de git (commit `b798bf6`).

Despliegue: el repositorio se publica tal cual en Vercel (Framework Preset *Other*, sin comando de compilación).
