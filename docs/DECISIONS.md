# Registro de decisiones

## Decisión 001 — Utilizar VILT

**Estado:** Aceptada.

**Contexto:** Se busca aprender backend y frontend en un proyecto Laravel coherente.

**Decisión:** Usar Vue, Inertia, Laravel y Tailwind.

**Razones:** Stack integrado, productivo y adecuado para recorrer una petición completa.

**Consecuencias:** Se aprenderán PHP/TypeScript y responsabilidades de servidor/cliente.

## Decisión 002 — Utilizar un monolito con Inertia

**Estado:** Aceptada.

**Contexto:** Las páginas normales no requieren dos aplicaciones desacopladas.

**Decisión:** Laravel resuelve HTTP y entrega páginas Vue mediante Inertia; no crear una API separada inicialmente.

**Razones:** Reduce complejidad incidental y mantiene visible el ciclo completo.

**Consecuencias:** Rutas, autorización y datos permanecen en Laravel.

## Decisión 003 — Codex como mentor

**Estado:** Aceptada.

**Contexto:** El objetivo principal es aprender.

**Decisión:** El usuario escribe progresivamente el código funcional; Codex prepara, explica, revisa y da pistas.

**Razones:** La práctica y la recuperación activa favorecen la comprensión.

**Consecuencias:** Las funcionalidades avanzan en pasos pequeños.

## Decisión 004 — Evitar sobrearquitectura

**Estado:** Aceptada.

**Contexto:** Todavía no existen necesidades de dominio que justifiquen capas adicionales.

**Decisión:** Seguir convenciones de Laravel e introducir abstracciones solo ante una necesidad real.

**Razones:** El código directo es más fácil de aprender, probar y cambiar.

**Consecuencias:** Eloquent será la opción inicial; no habrá repositorios genéricos.

## Decisión 005 — MySQL para desarrollo

**Estado:** Aceptada.

**Contexto:** Se necesita una base relacional habitual en proyectos Laravel.

**Decisión:** Usar MySQL local en desarrollo y mantener tests aislados con SQLite en memoria según el scaffold.

**Razones:** Permite aprender MySQL sin hacer dependientes de servicios externos a los tests.

**Consecuencias:** El servidor MySQL debe estar activo para migraciones locales; los tests usan su propia base efímera.
