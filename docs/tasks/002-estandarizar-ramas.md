# Tarea 002 — Estandarizar la numeración de ramas

**Estado:** En curso

**Rama:** `002-estandarizar-ramas`

**Fecha de inicio:** 2026-07-21

## Objetivo

Establecer que todas las ramas de trabajo comiencen por el número del plan correspondiente, facilitando la relación visual entre tarea, documentación, rama y commits.

## Qué se aprende

- Cómo una convención de nombres mejora la trazabilidad.
- Cómo relacionar una rama Git con su plan de trabajo.
- Por qué una convención debe ser concreta y verificable.

## Alcance

- Cambiar la convención global de ramas a `NNN-descripcion`.
- Aplicar la convención a esta misma tarea.
- Reordenar el recorrido VILT como Tarea 003.
- Actualizar README e índice de tareas.

## Fuera de alcance

- Modificar código funcional.
- Cambiar el flujo de autenticación.
- Iniciar el recorrido VILT.
- Crear ramas para todas las tareas futuras por adelantado.

## Pasos

- [x] Crear la rama `002-estandarizar-ramas`.
- [x] Actualizar la convención en el README.
- [x] Actualizar el índice de tareas.
- [x] Crear este plan.
- [x] Verificar que no quedan referencias a la convención anterior.
- [ ] Crear el commit de la tarea.
- [ ] Publicar la rama.

## Criterios de aceptación

- La rama comienza por `002`.
- README y `docs/TASKS.md` describen `NNN-descripcion`.
- La próxima tarea prevista tiene el número 003.
- No se ha modificado código funcional.

## Verificación

```bash
git branch --show-current
rg "task/NNN|feature/NNN" README.md docs
git diff --check
```
