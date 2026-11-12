# Picharreal Fantasy · landing

**Web:** <https://unaibermudez.github.io/picharreal-fantasy-landing/>

Landing pública de **Picharreal Fantasy**, la app privada de un equipo de fútbol 7 de la liga de Fútbol Rápido Bizkaia. Mezcla un fantasy entre compañeros (quinteto con presupuesto, capitán ×2, porra del partido y clasificaciones) con la gestión del equipo real (convocatoria, bajas, coches, caja y calendario). Los puntos salen solos del acta oficial de la liga y el partido se sigue en directo.

## Qué hay en este repo

Solo el build estático de la landing, en la rama `gh-pages`. Lo publica automáticamente un workflow de GitHub Actions del repositorio principal cada vez que cambia la landing.

## Por qué el código es privado

La app trabaja con datos de personas reales (jugadores, resultados y actas de la liga), así que su repositorio es privado y la app solo admite cuentas aprobadas. La landing es pública y **no muestra ningún dato real**: las capturas salen de un equipo inventado y una comprobación en la CI rompe el build si se cuela un nombre real.

## Stack

| Parte | Tecnología |
|---|---|
| App: backend | Go, PostgreSQL, OpenAPI (`oapi-codegen`), sqlc, River, Server-Sent Events |
| App: frontend | React, TypeScript, TanStack Router y Query, Tailwind, PWA |
| App: despliegue | AWS Lightsail, Docker Compose, Caddy, GitHub Actions |
| Landing | Astro, HTML y CSS estáticos, sin JavaScript |

Autor: [Unai Bermúdez](https://unaibermudez.github.io)
