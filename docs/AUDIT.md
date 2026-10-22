# Auditoría del estado real — 2026-10-22

Base local: commit `a2d329b`, repositorio CarloSol-90/LaraCode. Rama de origen `004-create-learning-path-model`; rama documental `005-align-master-plan`. Se conservaron los cambios locales de TASKS y el plan 004 aún no versionado. No se implementan funcionalidades ni se actualizan dependencias.

| Evidencia inspeccionada | Hallazgo |
| --- | --- |
| composer.json y composer.lock | Laravel 13, adaptador Inertia 3, Fortify, Wayfinder, Pest 4, Pint y Larastan. No hace falta migrar el stack. |
| package.json y package-lock.json | Vue 3, TypeScript, Inertia 3, Tailwind 4, Vite 8; scripts de lint, formato, tipos y build. |
| app/Models, database/migrations | Solo User y tablas de infraestructura/autenticación; no LearningPath ni dominio educativo. |
| routes/web.php y resources/js/pages | Welcome y Dashboard personalizados; dashboard declara auth/verified. |
| config/fortify.php, FortifyServiceProvider y ajustes | Registro, login, recuperación, configuración de verificación, 2FA y passkeys; conservar. |
| app/Models/User.php | MustVerifyEmail está comentado y User no implementa ese contrato. Declarar middleware verified no demuestra que el correo se exija realmente; revisar en tarea independiente, sin modificar auth aquí. |
| tests/Feature y tests/Unit | Pruebas existentes de autenticación, perfil, seguridad, dashboard y ejemplos; mayoritariamente clases PHPUnit aunque Pest está instalado. |
| .env.example y phpunit.xml | MySQL previsto para desarrollo, SQLite en memoria para tests. No se inspeccionan secretos ni se comprueba MySQL en vivo. |
| .github/workflows/tests.yml | CI para PR y main; prepara aplicación con SQLite, compila mediante composer setup y ejecuta composer ci:check. |
| docs/tasks/004-create-learning-path-model.md | Plan de persistencia sin implementación. El comando composer analyse no existe; corregido a composer types:check. |

## Conservar y corregir

Conservar autenticación, personalizaciones, tests, historial y convenciones. La documentación anterior posponía demasiado contenido profesional y carecía del contrato Exercises/Assessment. Se actualiza planificación para distinguir lo implementado, lo propuesto y lo pendiente de validar. No se deduce aprendizaje personal de una prueba superada.

La conversación recuperada solo expone un resumen y referencias opacas: los nombres exactos de los siete formatos y la fórmula adaptativa no se pueden atribuir al acuerdo previo. La lista del brief es propuesta; la fórmula queda pendiente. El alcance pedido sí incluye siete formatos, cinco niveles, dominio por habilidad y preparación profesional en MVP.

## Verificación

Resultados de esta ejecución en [VALIDATION.md](VALIDATION.md). Disponibilidad de herramientas no equivale a checks superados. Las afirmaciones históricas del diario pertenecen a sus sesiones originales.
