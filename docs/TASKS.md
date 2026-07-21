# Índice de tareas

Este documento es la fuente de verdad operativa del desarrollo de LaraCode. Solo debe existir una tarea funcional activa a la vez.

## Estados

- **Pendiente:** todavía no se ha comenzado.
- **En curso:** existe trabajo activo en su rama.
- **Completada:** cumple sus criterios, está verificada e integrada.
- **Bloqueada:** necesita una decisión o dependencia externa documentada.

## Convención

- Identificador: `NNN` con tres cifras.
- Plan: `docs/tasks/NNN-descripcion.md`.
- Rama: `NNN-descripcion`; el número del plan debe ser el primer elemento del nombre.
- Commit recomendado: `tipo(scope): descripción`.
- Cada plan debe incluir objetivo, aprendizaje, alcance, pasos, criterios de aceptación y verificaciones.

## Tareas

| ID | Tarea | Estado | Plan |
| --- | --- | --- | --- |
| 001 | Publicación inicial profesional | Completada | [Ver plan](tasks/001-publicacion-inicial.md) |
| 002 | Estandarizar la numeración de ramas | En curso | [Ver plan](tasks/002-estandarizar-ramas.md) |
| 003 | Recorrido guiado de una petición VILT | Pendiente | Por crear al iniciar la tarea |

## Regla de enfoque

No se añaden varias funcionalidades a una misma tarea. Si aparece trabajo nuevo durante una tarea, se registra como una tarea posterior en lugar de ampliar silenciosamente el alcance.

Ejemplos válidos: `002-estandarizar-ramas`, `003-recorrido-peticion-vilt`. Ejemplos no válidos: `task/003-recorrido-peticion-vilt`, `feature/003-recorrido-peticion-vilt`.
