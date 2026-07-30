# Diario de desarrollo

Este documento registra lo aprendido durante la construcción de LaraCode.

## Plantilla

### Sesión N — Título

**Fecha:**

**Objetivo:**

**Conceptos aprendidos:**

-

**Código que escribí:**

-

**Errores encontrados:**

-

**Cómo los resolví:**

-

**Qué todavía no entiendo:**

-

**Próximo paso:**

-

## Sesión 0 — Preparación del entorno

**Fecha:** 2026-07-20

**Objetivo:** Dejar un scaffold VILT oficial y documentado, sin crear dominio propio.

**Herramientas preparadas:** Laravel 13, Vue 3, Inertia 3, Tailwind 4, TypeScript, Vite, Fortify, Pest, Pint, Boost, ESLint y Prettier. MySQL 8 quedó conectado con la base `laracode` y las migraciones iniciales.

**Comandos ejecutados:** inspección de versiones/extensiones; actualización de Composer; instalación del Laravel Installer; creación con `laravel new` y opciones Vue/Pest/MySQL/npm/Boost/Git; `php artisan migrate`; `php artisan test` (39 tests y 136 assertions); Pint; ESLint; Prettier; Vue TSC; PHPStan; `npm run build`; y comprobación HTTP temporal con respuesta 200.

**Próximo paso:** Recorrer carpetas y seguir una petición desde una ruta Laravel hasta una página Vue. No se atribuyen todavía conceptos aprendidos al alumno.

## Sesión 1 — Seguir una petición VILT

**Fecha:** 2026-07-30

**Objetivo:** Comprender el recorrido de `/dashboard` y realizar el primer cambio visible y probado sobre una página Inertia.

**Conceptos aprendidos:**

- Una ruta existente protegida por `auth` redirige al login; no devuelve un 404.
- `verified` detiene a un usuario autenticado cuyo correo todavía no está verificado.
- En `Route::inertia('dashboard', 'Dashboard')->name('dashboard')`, la URI, la página Vue y el nombre interno de la ruta son conceptos distintos.
- Inertia 3 resuelve `Dashboard` como `resources/js/pages/Dashboard.vue`, y `app.ts` le asigna `AppLayout` mediante el caso por defecto.
- `HandleInertiaRequests` comparte `auth.user` con las páginas Vue.
- Un test de endpoint puede comprobar el componente Inertia y sus props con `assertInertia`.

**Código que escribí:**

- Un bloque de bienvenida en el dashboard que muestra el nombre del usuario autenticado mediante `$page.props.auth.user.name`.
- Aserciones en `DashboardTest` para comprobar el componente `Dashboard` y las props `auth.user.id` y `auth.user.name`.
- Configuración de VS Code para aplicar Prettier al guardar archivos Vue, TypeScript y JavaScript.

**Errores encontrados:**

- Se confundió inicialmente una ruta protegida con una ruta inexistente.
- El código PHP y Vue contenía tabulaciones e indentación irregular.
- El build no pudo crear un archivo temporal de Vite dentro del sandbox.

**Cómo los resolví:**

- Se distinguieron las respuestas 404 de las redirecciones producidas por middleware.
- Prettier y Pint corrigieron el formato según el tipo de archivo.
- El build se repitió con permiso para escribir el temporal y finalizó correctamente.

**Qué todavía no entiendo:**

- Queda por observar en Network la diferencia entre una carga completa del documento y una visita interna de Inertia.

**Verificación:**

- Ruta `/dashboard` registrada correctamente.
- Pint completado.
- 39 tests y 147 aserciones superados.
- ESLint, Prettier y comprobación de tipos superados.
- Build de producción completado.

**Próximo paso:**

- Crear la primera ruta de aprendizaje, `Laravel desde cero`, como inicio del dominio educativo de LaraCode.
