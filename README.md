# LaraCode

> Aprende Laravel programando.

LaraCode es una aplicación web educativa y gamificada que se construirá progresivamente para aprender desarrollo full stack. Es, al mismo tiempo, el proyecto de aprendizaje y la futura herramienta para seguir aprendiendo Laravel. Estado actual: **preparación inicial**; todavía no existe dominio propio.

## Objetivos

- Aprender el stack VILT (Vue, Inertia, Laravel y Tailwind).
- Crear una plataforma práctica para aprender Laravel.
- Construir poco a poco, sin delegar todo el código funcional a la IA.

## Stack instalado

| Tecnología | Versión instalada | Responsabilidad |
| --- | ---: | --- |
| PHP | 8.4.20 | Lenguaje del backend |
| Laravel | 13.20.0 | Framework, rutas, HTTP, Eloquent y servicios |
| Vue | 3.5.40 | Interfaz mediante Composition API |
| Inertia | 3.1.1 / Vue 3.6.1 | Une Laravel y Vue sin API separada |
| Tailwind CSS | 4.3.3 | Estilos utilitarios |
| TypeScript | 5.9.3 | Tipado del frontend |
| Vite | 8.1.5 | Desarrollo y compilación de recursos |
| MySQL | 8.0.30 | Persistencia de desarrollo |
| Pest | 4.7.5 | Tests |
| Laravel Pint | 1.29.3 | Formato PHP |
| Laravel Boost | 2.4.13 | Contexto, guías, skills y MCP para Codex |

El starter kit también incluye Fortify 1.37.2 para autenticación, ESLint 9.39.5, Prettier 3.9.5, Vue TSC 2.2.12, Wayfinder y componentes shadcn-vue/Reka UI oficiales del scaffold.

## Requisitos

- PHP 8.3 o posterior con PDO MySQL, mbstring, openssl, tokenizer, XML, ctype, curl, fileinfo y bcmath.
- Composer 2 (detectado: 2.10.2).
- Node.js compatible con Vite 8; usar una versión LTS vigente compatible. Detectado: 24.15.0.
- npm compatible (detectado: 11.12.1).
- MySQL 8 o compatible (detectado: 8.0.30).
- Git (detectado: 2.37.3).

## Instalación

```bash
git clone <url-del-repositorio> laracode
cd laracode
composer install
npm install
copy .env.example .env
php artisan key:generate
```

En macOS/Linux, sustituye `copy` por `cp`. Configura en `.env` las variables `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME` y `DB_PASSWORD`. Crea la base desde un cliente MySQL:

```sql
CREATE DATABASE laracode CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

Después:

```bash
php artisan migrate
npm run build
```

## Desarrollo

Terminal del backend:

```bash
php artisan serve
```

Terminal del frontend:

```bash
npm run dev
```

El comando combinado oficial también inicia el listener de colas:

```bash
composer run dev
```

## Calidad

```bash
php artisan test
vendor/bin/pint
npm run lint:check
npm run format:check
npm run types:check
npm run build
```

En Windows puede ejecutarse Pint con `vendor\bin\pint.bat`. `composer test` agrupa Pint, Larastan y los tests de backend.

## Estructura relevante

- `app/`: código PHP y acciones/controladores del scaffold.
- `config/`: configuración de Laravel y Fortify.
- `database/`: migraciones, factories y seeders iniciales.
- `resources/js/`: páginas, layouts y componentes Vue/TypeScript.
- `resources/css/`: entrada de Tailwind.
- `routes/`: rutas web, autenticación/settings y consola.
- `tests/`: tests Pest unitarios y de feature.
- `docs/`: visión, arquitectura, aprendizaje y decisiones.
- `.agents/` y `.codex/`: integración generada por Boost.

## Arquitectura VILT

El navegador visita una ruta Laravel; middleware y controlador procesan la petición; Eloquent accederá a MySQL cuando haya datos; Inertia entrega props a una página Vue; Vue renderiza la interfaz y Tailwind la presenta. No hay una API REST separada para las páginas normales.

## Autenticación

El starter kit oficial usa Laravel Fortify e incluye registro, inicio/cierre de sesión, recuperación de contraseña, verificación de correo, confirmación de contraseña, autenticación de dos factores, passkeys y ajustes de perfil/seguridad. No hay usuarios ni credenciales ficticias.

## Estado

Implementado:

- Entorno base y starter kit VILT.
- Autenticación base.
- Tests iniciales y herramientas de calidad.
- Integración de Laravel Boost.
- Documentación inicial.

Pendiente:

- Diseño funcional y dominio.
- Cursos, lecciones, ejercicios y progreso.
- Gamificación y administración.
- PWA.

## Filosofía educativa

Codex es un mentor. Las funcionalidades se dividen en pasos pequeños: primero explicación y diagnóstico, después código escrito por el alumno, revisión, pistas y tests. La velocidad no sustituye a la comprensión.

## Próximo paso

> Recorrer y comprender el proyecto generado antes de crear funcionalidades.
