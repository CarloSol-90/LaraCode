# Arquitectura

## Estado inicial

LaraCode es un monolito Laravel 13. La interfaz usa Vue 3 y TypeScript; Inertia 3 conecta las rutas/controladores con las páginas Vue; Tailwind CSS 4 aporta estilos y Vite 8 compila recursos. MySQL será la persistencia de desarrollo. Pest ejecuta tests, Pint formatea PHP y Laravel Boost aporta a Codex contexto específico de las versiones instaladas.

No existe una API REST separada para las páginas normales.

## Flujo conceptual de una petición

```text
Usuario pulsa un enlace
→ Vue/Inertia realiza la visita
→ Laravel resuelve la ruta y aplica middleware
→ Un controlador prepara los datos (Eloquent/MySQL cuando proceda)
→ Inertia envía las props
→ Vue renderiza la página con estilos Tailwind
```

Este flujo solo describe la arquitectura; no representa una funcionalidad propia ya creada.

## Decisiones que todavía no se han tomado

- Modelo definitivo de cursos.
- Sistema de progreso.
- Repetición espaciada.
- Gestión de contenido.
- Estrategia PWA.
- Ejecución futura y segura de ejercicios de código.
