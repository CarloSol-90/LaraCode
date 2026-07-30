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
