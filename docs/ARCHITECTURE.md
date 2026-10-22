# Arquitectura

## Base comprobada

Monolito Laravel 13, Vue 3 con TypeScript, Inertia 3, Tailwind 4 y Vite 8. Fortify conserva autenticación, 2FA y soporte de passkeys. MySQL es el objetivo de desarrollo en `.env.example`; `phpunit.xml` usa SQLite en memoria. Pest 4 está instalado, aunque los tests existentes usan mayoritariamente clases PHPUnit. No existe API separada para las páginas normales ni dominio educativo implementado.

Flujo: ruta Laravel → middleware → controlador o respuesta Inertia directa → props → página Vue. `routes/web.php` entrega Dashboard; `HandleInertiaRequests` comparte el usuario.

## Monolito modular como dirección

Estos son límites conceptuales, no carpetas que crear ahora. Se conserva la estructura Laravel existente y se agrupa código cuando una funcionalidad real lo necesite.

| Área | Responsabilidad y límites |
| --- | --- |
| Identity | Usuarios y acceso existentes; conservar Fortify. Cada área autoriza sus recursos. |
| Learning | Rutas, cursos, módulos, lecciones y avance de contenido; no calcula dominio. |
| Exercises | Enunciados, siete formatos, soluciones/rúbricas, versiones e intentos; produce evidencia y feedback. |
| Assessment | Habilidades, dominio 0–100, cinco niveles y recomendaciones; consume evidencia, no define ni renderiza formatos. |
| Knowledge | LaraCodepedia pública gratuita, referencias oficiales y versiones. |
| CareerPractice | Casos, entrevistas y pruebas prácticas; compone ejercicios y rúbricas sin duplicar el motor. |
| Gamification | Puntos y logros; nunca altera artificialmente el dominio. |
| Entitlements, futuro | Posible Free/Pro, sin facturación en MVP. |

## Modelo conceptual, todavía sin esquema físico

Tecnología → ruta → curso → módulo → lección. Las lecciones enlazan ejercicios y conceptos. Un ejercicio puede aportar evidencia para varias habilidades mediante relaciones explícitas; ponderación pendiente. Un intento pertenece a un usuario y una versión del ejercicio, con respuesta, feedback y estado de revisión. Casos y sesiones de entrevista/prueba agrupan ejercicios.

Separar avance de contenido, dominio por habilidad y puntuación lúdica. No guardar progreso individual en la tabla de rutas. La tarea 004 sigue limitada a persistencia de LearningPath; no crear todo el grafo de entidades de una vez.

## Contrato Exercises / Assessment

Exercises valida entregas y produce un resultado estructurado: identificadores de intento, usuario y versión del ejercicio, habilidades, dificultad, corrección o rúbrica, revisión pendiente y ayudas usadas. Assessment acepta evidencia evaluada, evita contar dos veces un intento y conserva versión de política y trazabilidad de cambios.

Una repetición o ayuda no equivale automáticamente a evidencia independiente. Dificultad 1–5 no se obtiene dividiendo dominio en cinco tramos. Sin evidencia se informa sin evaluar. La selección siguiente cubre habilidad y dificultad apropiadas con alternativa si falta contenido. Umbrales, repeticiones y tratamiento de errores se acordarán con ejemplos y tests antes de implementar. Empezar con reglas deterministas comprensibles, sin ML ni promesas psicométricas.

## SOLID pragmático

Controladores coordinan HTTP; Form Requests validan y Policies autorizan cuando corresponda. Eloquent es la persistencia inicial. Extraer una Action o servicio ante reglas complejas o reutilizadas, por ejemplo una política de evaluación. Introducir interfaces ante implementaciones intercambiables reales, no por cada modelo. Evitar repositorios genéricos, jerarquías por formato y buses de eventos prematuros. Vue usa Composition API y `<script setup>`; estado de página primero, composables ante reutilización real y sin Pinia preventivo.

## Seguridad y calidad previstas

Corrección y puntuación se resuelven en servidor; no confiar en puntos del navegador. Autorizar intentos y progreso por usuario. Sanear contenido y revisar aportaciones abiertas. No ejecutar código arbitrario: soluciones abiertas se preparan fuera de plataforma y revisan con rúbrica en MVP. No enviar datos personales a terceros por defecto.

Pruebas de acceso, persistencia y recorrido; pruebas unitarias de política para límites 0–100, ausencia de evidencia, cambios de dificultad y duplicados. SQLite agiliza tests; restricciones dependientes del motor requerirán comprobación MySQL en su tarea. AWS queda fuera de la ejecución inicial.

## Pendiente

Taxonomía final de formatos, esquema de habilidades, rúbricas, política adaptativa, umbrales, autoría/publicación, criterios de logros y posible Pro. No introducir tablas ni servicios vacíos para representar decisiones pendientes.
