# Tarea 001 — Publicación inicial profesional

**Estado:** En curso

**Rama:** `main` (publicación inicial excepcional)

**Fecha de inicio:** 2026-07-21

## Objetivo

Publicar por primera vez LaraCode en GitHub con una presentación profesional, documentación clara y una forma sostenible de organizar el trabajo futuro.

## Qué se aprende

- Diferencia entre repositorio local y remoto.
- Relación entre rama, commit y push.
- Cómo presentar técnicamente un proyecto en un README.
- Cómo limitar y verificar una tarea antes de integrarla.

## Alcance

- Integrar el logo en la Welcome y en el README.
- Mejorar el README principal.
- Crear el índice y la convención de tareas.
- Documentar esta primera tarea.
- Validar el estado actual.
- Configurar el remoto indicado y publicar `main`.

## Fuera de alcance

- Crear funcionalidades del dominio.
- Rediseñar autenticación o dashboard.
- Configurar CI/CD.
- Publicar la aplicación en un servidor.

## Pasos

- [x] Preparar el proyecto base VILT.
- [x] Personalizar Welcome con la identidad de LaraCode.
- [x] Incorporar el logo como asset versionado.
- [x] Redactar un README orientado a portfolio.
- [x] Definir la organización de tareas.
- [x] Ejecutar tests y comprobaciones de calidad.
- [x] Revisar los archivos que entrarán en el commit.
- [x] Configurar `origin` con el repositorio correcto.
- [ ] Crear el commit de la tarea.
- [ ] Publicar `main` y verificar el upstream.

## Criterios de aceptación

- El README explica propósito, stack, arquitectura, instalación y estado real.
- El logo se visualiza en GitHub mediante una ruta relativa.
- Existe un índice de tareas enlazado desde el README.
- `.env`, dependencias y builds locales no se publican.
- Tests, lint, tipos y build terminan correctamente.
- `main` queda publicada en `git@github.com:CarloSol-90/LaraCode.git`.
- El repositorio no contiene funcionalidades propias no acordadas.

## Verificaciones previstas

```bash
php artisan test
vendor/bin/pint --dirty
npm run lint:check
npm run format:check
npm run types:check
npm run build
git status
```

## Resultado

Se completará tras validar el push y se registrarán aquí el commit publicado y cualquier incidencia real.
