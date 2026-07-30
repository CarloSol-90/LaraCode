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

- Modelo físico definitivo de rutas, cursos y prerrequisitos.
- Sistema de progreso.
- Repetición espaciada.
- Gestión de contenido.
- Estrategia PWA.
- Ejecución futura y segura de ejercicios de código.

## Modelo educativo conceptual

La arquitectura del dominio distinguirá conceptos educativos en lugar de asumir que todo contenido es un lenguaje de programación:

```text
Tecnología
└── Ruta de aprendizaje
    └── Curso
        └── Módulo
            └── Lección
                └── Ejercicio
```

Laravel es un framework de PHP y será la tecnología principal del producto inicial. El sistema no debe introducir condiciones específicas como `if course is Laravel`; Laravel será contenido inicial dentro de estructuras reutilizables.

En fases posteriores, un curso podrá depender de otros cursos. Una ruta de Laravel + Vue, por ejemplo, podrá requerir haber completado previamente los cursos de Laravel y Vue. Esta relación de prerrequisitos no se implementará hasta que existan al menos dos cursos que necesiten conectarse.
