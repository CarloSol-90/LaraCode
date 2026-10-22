# Task 004 — Create the learning path data model

## Objective

Design and implement the first domain entity in LaraCode: a learning path. This task covers only persistence and automated tests, establishing a small, reliable foundation before adding HTTP routes or user interface code.

## Objetivo

Diseñar e implementar la primera entidad de dominio de LaraCode: una ruta de aprendizaje. Esta tarea cubre únicamente la persistencia y los tests automatizados, creando una base pequeña y fiable antes de añadir rutas HTTP o interfaz de usuario.

## Learning goals

- Distinguish a database table, an Eloquent model, and a model factory.
- Choose column types, nullability, defaults, and indexes intentionally.
- Understand why a slug is different from a display name and must be unique.
- Test database behavior with Pest and an isolated test database.

## Objetivos de aprendizaje

- Diferenciar una tabla de base de datos, un modelo Eloquent y una factory.
- Elegir conscientemente tipos de columna, nulabilidad, valores por defecto e índices.
- Comprender por qué un slug es distinto de un nombre visible y debe ser único.
- Probar el comportamiento de la base de datos con Pest y una base aislada para tests.

## Scope

- Define the minimum attributes for a learning path.
- Create the `learning_paths` migration.
- Create the `LearningPath` model.
- Create the `LearningPathFactory` factory.
- Add focused Pest tests for persistence, defaults, casts, and uniqueness where appropriate.
- Update the related project documentation after the implementation is verified.

## Alcance

- Definir los atributos mínimos de una ruta de aprendizaje.
- Crear la migración de `learning_paths`.
- Crear el modelo `LearningPath`.
- Crear la factory `LearningPathFactory`.
- Añadir tests Pest enfocados en persistencia, valores por defecto, casts y unicidad cuando corresponda.
- Actualizar la documentación relacionada después de verificar la implementación.

## Out of scope

- Controllers, routes, Inertia pages, and Vue components.
- CRUD forms and validation.
- Courses, modules, lessons, exercises, and relationships.
- User progress, publication workflows, and administration.
- Seeders unless a concrete need appears during the task.

## Fuera de alcance

- Controladores, rutas, páginas Inertia y componentes Vue.
- Formularios CRUD y validación.
- Cursos, módulos, lecciones, ejercicios y relaciones.
- Progreso del usuario, flujos de publicación y administración.
- Seeders salvo que aparezca una necesidad concreta durante la tarea.

## Planned steps

1. Agree on the attributes and database constraints.
2. Generate the model, migration, and factory with Artisan.
3. Write the migration and model behavior in small steps.
4. Define realistic factory defaults.
5. Add focused database tests with Pest.
6. Run the relevant tests, Pint, static analysis, and the project quality checks.
7. Record the learning evidence and mark the task complete only after verification.

## Pasos previstos

1. Acordar los atributos y restricciones de base de datos.
2. Generar el modelo, la migración y la factory con Artisan.
3. Escribir la migración y el comportamiento del modelo en pasos pequeños.
4. Definir valores realistas en la factory.
5. Añadir tests de base de datos enfocados con Pest.
6. Ejecutar los tests relacionados, Pint, análisis estático y las comprobaciones de calidad del proyecto.
7. Registrar la evidencia de aprendizaje y marcar la tarea como completada solo después de verificarla.

## Acceptance criteria

- The schema represents the agreed learning path attributes and constraints.
- `LearningPath` follows Laravel naming and Eloquent conventions.
- The factory can persist valid learning paths for tests.
- Focused Pest tests demonstrate the intended database behavior.
- No HTTP or frontend functionality is introduced.
- All relevant verification commands pass.

## Criterios de aceptación

- El esquema representa los atributos y restricciones acordados para la ruta de aprendizaje.
- `LearningPath` sigue las convenciones de nombres y de Eloquent de Laravel.
- La factory puede persistir rutas de aprendizaje válidas para los tests.
- Tests Pest enfocados demuestran el comportamiento previsto de la base de datos.
- No se introduce funcionalidad HTTP ni frontend.
- Todas las comprobaciones relevantes terminan correctamente.

## Verification commands

```bash
php artisan test --compact --filter=LearningPath
vendor/bin/pint --dirty --format agent
composer types:check
composer ci:check
```

## Comandos de verificación

Los comandos anteriores ejecutan los tests específicos, aplican el formato PHP, realizan el análisis estático y terminan con la comprobación completa del proyecto.
