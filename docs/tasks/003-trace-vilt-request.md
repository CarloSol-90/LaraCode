# Task 003 — Trace a VILT request

# Tarea 003 — Seguir una petición VILT

**Status:** In progress

**Estado:** En curso

**Branch:** `003-trace-vilt-request`

**Rama:** `003-trace-vilt-request`

**Start date:** 2026-07-21

**Fecha de inicio:** 2026-07-21

## Objective

Understand the complete path of a request from the browser to a Laravel route and middleware, through Inertia, and finally to a Vue page component.

## Objetivo

Comprender el recorrido completo de una petición desde el navegador hasta una ruta y middleware de Laravel, pasando por Inertia y terminando en un componente de página Vue.

## Learning goals

- Identify which layer decides the requested page.
- Understand the role of a Laravel route.
- Distinguish authentication middleware from page rendering.
- Understand how Inertia resolves a Vue page component.
- Identify shared and page-specific props.
- Explain the difference between a full page load and an Inertia visit.

## Objetivos de aprendizaje

- Identificar qué capa decide la página solicitada.
- Comprender la función de una ruta de Laravel.
- Diferenciar el middleware de autenticación del renderizado de la página.
- Comprender cómo Inertia resuelve un componente de página Vue.
- Identificar props compartidas y específicas de una página.
- Explicar la diferencia entre una carga completa y una visita de Inertia.

## Request flow

```text
Browser
→ Laravel route
→ auth and verified middleware
→ Inertia page response
→ shared and page props
→ Vue page resolver
→ Dashboard.vue
→ rendered HTML
```

## Recorrido de la petición

```text
Navegador
→ ruta de Laravel
→ middleware auth y verified
→ respuesta de página Inertia
→ props compartidas y de página
→ resolución de la página Vue
→ Dashboard.vue
→ HTML renderizado
```

## Files to study

- `routes/web.php`
- `bootstrap/app.php`
- `app/Http/Middleware/HandleInertiaRequests.php`
- `resources/js/app.ts`
- `resources/js/pages/Dashboard.vue`
- `resources/js/types/index.ts`

## Archivos que estudiaremos

- `routes/web.php`
- `bootstrap/app.php`
- `app/Http/Middleware/HandleInertiaRequests.php`
- `resources/js/app.ts`
- `resources/js/pages/Dashboard.vue`
- `resources/js/types/index.ts`

## Scope

- Read and explain the existing dashboard request flow.
- Inspect the route and middleware configuration.
- Inspect Inertia bootstrapping and page resolution.
- Observe the request in the browser developer tools.
- Complete one small guided change after the flow is understood.
- Add or update a focused test for that change.

## Alcance

- Leer y explicar el flujo existente de la petición al dashboard.
- Inspeccionar la configuración de la ruta y los middleware.
- Inspeccionar el arranque de Inertia y la resolución de páginas.
- Observar la petición en las herramientas de desarrollo del navegador.
- Completar un pequeño cambio guiado después de comprender el flujo.
- Añadir o actualizar un test específico para ese cambio.

## Out of scope

- Creating courses, lessons, exercises, or other domain models.
- Replacing the starter-kit authentication.
- Creating a separate API.
- Redesigning the dashboard.
- Adding new dependencies.

## Fuera de alcance

- Crear cursos, lecciones, ejercicios u otros modelos del dominio.
- Reemplazar la autenticación del starter kit.
- Crear una API separada.
- Rediseñar el dashboard.
- Añadir dependencias.

## Steps

- [x] Create the branch from updated `main`.
- [x] Create the bilingual task plan.
- [x] Initialize the project glossary and practical code-reading guide.
- [x] Read the dashboard route.
- [x] Identify the middleware and predict their behavior.
- [x] Follow Inertia page resolution in `resources/js/app.ts`.
- [x] Inspect shared props in `HandleInertiaRequests`.
- [x] Inspect `Dashboard.vue` and its layout.
- [ ] Observe a dashboard visit in the browser network panel.
- [x] Implement one small guided change.
- [x] Add or update the focused test.
- [x] Run quality checks and build.
- [x] Update the learning journal.
- [ ] Commit, push, review, and merge the task.

## Pasos

- [x] Crear la rama desde `main` actualizado.
- [x] Crear el plan bilingüe de la tarea.
- [x] Inicializar el glosario del proyecto y la guía práctica de lectura de código.
- [x] Leer la ruta del dashboard.
- [x] Identificar los middleware y predecir su comportamiento.
- [x] Seguir la resolución de páginas de Inertia en `resources/js/app.ts`.
- [x] Inspeccionar las props compartidas en `HandleInertiaRequests`.
- [x] Inspeccionar `Dashboard.vue` y su layout.
- [ ] Observar una visita al dashboard en el panel de red del navegador.
- [x] Implementar un pequeño cambio guiado.
- [x] Añadir o actualizar el test específico.
- [x] Ejecutar las comprobaciones de calidad y el build.
- [x] Actualizar el diario de aprendizaje.
- [ ] Confirmar, publicar, revisar y fusionar la tarea.

## Acceptance criteria

- The complete dashboard request flow can be explained without guessing.
- The purpose of `auth` and `verified` is understood.
- The relationship between the route name and the Vue page name is clear.
- Shared props and page-specific props can be distinguished.
- The guided change is small, tested, and does not introduce domain code.
- Documentation and checks are up to date.

## Criterios de aceptación

- Se puede explicar el flujo completo de la petición al dashboard sin adivinar.
- Se comprende el propósito de `auth` y `verified`.
- Está clara la relación entre el nombre de la ruta y el nombre de la página Vue.
- Se pueden diferenciar las props compartidas de las específicas de página.
- El cambio guiado es pequeño, está probado y no introduce código de dominio.
- La documentación y las comprobaciones están actualizadas.

## Verification

```bash
php artisan route:list --path=dashboard
php artisan test --compact
npm run lint:check
npm run format:check
npm run types:check
npm run build
git diff --check
```

## Verificación

Se comprobarán la ruta del dashboard, los tests de Laravel, lint, formato, tipos, build y limpieza del diff antes de finalizar la tarea.

## Deferred review / Repaso aplazado

The browser Network comparison between a full document load and an Inertia visit was intentionally deferred. It remains a learning review item, but does not block the verified dashboard change from being integrated.

La comparación en Network entre una carga completa del documento y una visita de Inertia se aplazó intencionadamente. Permanece como punto de repaso, pero no bloquea la integración del cambio verificado del dashboard.
