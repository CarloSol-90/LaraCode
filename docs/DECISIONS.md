# Registro de decisiones

## Decisión 001 — Utilizar VILT

**Estado:** Aceptada.

**Contexto:** Se busca aprender backend y frontend en un proyecto Laravel coherente.

**Decisión:** Usar Vue, Inertia, Laravel y Tailwind.

**Razones:** Stack integrado, productivo y adecuado para recorrer una petición completa.

**Consecuencias:** Se aprenderán PHP/TypeScript y responsabilidades de servidor/cliente.

## Decisión 002 — Utilizar un monolito con Inertia

**Estado:** Aceptada.

**Contexto:** Las páginas normales no requieren dos aplicaciones desacopladas.

**Decisión:** Laravel resuelve HTTP y entrega páginas Vue mediante Inertia; no crear una API separada inicialmente.

**Razones:** Reduce complejidad incidental y mantiene visible el ciclo completo.

**Consecuencias:** Rutas, autorización y datos permanecen en Laravel.

## Decisión 003 — Codex como mentor

**Estado:** Aceptada.

**Contexto:** El objetivo principal es aprender.

**Decisión:** El usuario escribe progresivamente el código funcional; Codex prepara, explica, revisa y da pistas.

**Razones:** La práctica y la recuperación activa favorecen la comprensión.

**Consecuencias:** Las funcionalidades avanzan en pasos pequeños.

## Decisión 004 — Evitar sobrearquitectura

**Estado:** Aceptada.

**Contexto:** Todavía no existen necesidades de dominio que justifiquen capas adicionales.

**Decisión:** Seguir convenciones de Laravel e introducir abstracciones solo ante una necesidad real.

**Razones:** El código directo es más fácil de aprender, probar y cambiar.

**Consecuencias:** Eloquent será la opción inicial; no habrá repositorios genéricos.

## Decisión 005 — MySQL para desarrollo

**Estado:** Aceptada.

**Contexto:** Se necesita una base relacional habitual en proyectos Laravel.

**Decisión:** Usar MySQL local en desarrollo y mantener tests aislados con SQLite en memoria según el scaffold.

**Razones:** Permite aprender MySQL sin hacer dependientes de servicios externos a los tests.

**Consecuencias:** El servidor MySQL debe estar activo para migraciones locales; los tests usan su propia base efímera.

## Decisión 006 — Laravel primero, plataforma extensible después

**Estado:** Aceptada.

**Contexto:** LaraCode se inspira en una experiencia de aprendizaje progresiva y práctica. Laravel será el contenido principal, pero el producto podrá enseñar otras tecnologías en el futuro. Laravel es un framework de PHP, por lo que el dominio no debe confundir frameworks y lenguajes.

**Decisión:** Modelar conceptualmente tecnologías, rutas, cursos, módulos, lecciones y ejercicios como elementos diferenciados. El alcance inicial incluirá únicamente `Laravel desde cero`. Laravel será contenido inicial, no una condición especial escrita en la lógica de la aplicación.

**Razones:** Permite mantener un MVP enfocado sin impedir que posteriormente se incorporen PHP, Vue, JavaScript u otras tecnologías.

**Consecuencias:** No se implementarán todavía múltiples tecnologías, prerrequisitos, desbloqueos ni rutas combinadas. Cuando existan varios cursos, los prerrequisitos se representarán mediante relaciones entre cursos; por ejemplo, Laravel y Vue podrán desbloquear una ruta combinada de Laravel + Vue.

## Decisión 007 — Contrato del MVP ampliado

**Estado:** Aceptada por la petición de 2026-10-22; concreta y amplía el alcance inicial de la decisión 006.

**Decisión:** Formación Laravel primero, casos profesionales, siete formatos, evaluación adaptativa de cinco niveles, dominio 0–100 por habilidad, LaraCodepedia gratuita, entrevistas técnicas, pruebas prácticas y gamificación básica dentro del MVP.

**Consecuencias:** Entrega por incrementos; el primer recorrido no es todo el MVP. Los nombres concretos de formatos son propuesta pendiente de validar y la fórmula de evaluación queda pendiente. No se infieren de referencias opacas de la conversación anterior.

## Decisión 008 — Separar Exercises y Assessment

**Estado:** Aceptada como límite conceptual, sin módulos físicos todavía.

**Decisión:** Exercises gestiona práctica y evidencia; Assessment estima dominio y recomienda. Progreso, dominio y puntos son medidas distintas. Sin evidencia significa sin evaluar.

**Consecuencias:** Política determinista, trazable y versionada antes de automatismos complejos. Umbrales y fórmula requieren tarea con ejemplos y tests. No prometer certificación ni validez psicométrica.

## Decisión 009 — Modularidad y SOLID pragmáticos

**Estado:** Aceptada; desarrolla las decisiones 002 y 004.

**Decisión:** Mantener monolito Laravel 13 + Vue 3/TS + Inertia 3 + Tailwind 4 + MySQL + Pest; conservar estructura y autenticación. Extraer responsabilidades cuando el código real lo justifique.

**Consecuencias:** Sin carpetas vacías, microservicios, API separada, repositorios genéricos ni interfaces por rutina. Las dependencias ya satisfacen las versiones mayores objetivo; no actualizarlas en esta tarea documental.

## Decisión 010 — Aprendizaje guiado con delegación explícita

**Estado:** Aceptada; precisa la decisión 003.

**Decisión:** El autor practica decisiones y reglas esenciales; Codex prepara tareas repetitivas autorizadas y revisa. La petición actual autoriza ejecutar la actualización documental completa.

**Consecuencias:** Mantener preguntas diagnósticas y evidencias; no exigir que el autor redacte manualmente toda la documentación ni confundir código generado con comprensión.

## Decisión 011 — Referencias y producto futuro

**Estado:** Aceptada.

**Decisión:** Contenidos con fuentes oficiales asociadas a versión y fecha/revisión. LaraCodepedia gratuita. Free/Pro queda futuro, sin precios ni cobros; AWS será laboratorio posterior.

**Consecuencias:** Revisar compatibilidad al actualizar contenido; no copiar documentación íntegra ni aprovisionar infraestructura ahora. Propuestas comerciales y límites de costes requieren decisiones específicas.
