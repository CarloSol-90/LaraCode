# Glosario y guía práctica de código

Este es un documento vivo. Recoge términos que aparecen realmente durante la construcción de LaraCode y se ampliará cuando estudiemos conceptos nuevos.

## Glosario alfabético

### A

**API (Application Programming Interface)**
Contrato que permite que dos sistemas se comuniquen. LaraCode no utiliza inicialmente una API REST separada para sus páginas normales: Laravel e Inertia trabajan juntos dentro del mismo monolito.

**Artisan**
Interfaz de línea de comandos de Laravel. Se utiliza mediante `php artisan`. Permite consultar rutas, ejecutar migraciones, crear archivos y lanzar tests, entre otras tareas.

**Autenticación (`auth`)**
Proceso de comprobar quién es un usuario. El middleware `auth` impide acceder a rutas protegidas sin haber iniciado sesión.

### B

**Backend**
Parte de la aplicación que se ejecuta en el servidor. En LaraCode incluye PHP, Laravel, rutas, middleware, validación, Eloquent y acceso a MySQL.

**Base de datos**
Sistema que almacena información persistente. LaraCode utiliza MySQL durante el desarrollo y SQLite en memoria durante los tests.

**Branch (rama)**
Línea de trabajo independiente en Git. En LaraCode comienza por el número de su tarea, por ejemplo `003-trace-vilt-request`.

**Build**
Proceso que transforma y optimiza el frontend para producción. En este proyecto se ejecuta con `npm run build`.

### C

**Clase**
Plantilla de PHP que agrupa estado y comportamiento. Puede contener propiedades y métodos y utilizarse para crear objetos.

**CLI (Command-Line Interface)**
Interfaz controlada mediante comandos de terminal. Artisan, Git, Composer y npm ofrecen una CLI.

**Commit**
Registro permanente de un conjunto intencional de cambios en Git. Debe tener un mensaje breve que explique su propósito.

**Component (componente)**
Unidad reutilizable de una interfaz Vue. Agrupa template, comportamiento y, cuando es necesario, estilos.

**Composer**
Gestor de dependencias de PHP. Lee `composer.json` e instala paquetes dentro de `vendor/`.

**Controller (controlador)**
Clase de Laravel que recibe una petición y coordina su respuesta. No todas las rutas necesitan uno; una ruta sencilla puede devolver directamente una página de Inertia.

**CSRF (Cross-Site Request Forgery)**
Ataque que intenta ejecutar acciones en nombre de un usuario autenticado. Laravel protege los formularios mediante tokens CSRF.

### D

**Dependency (dependencia)**
Paquete o módulo que el proyecto necesita. Las dependencias PHP se gestionan con Composer y las JavaScript con npm.

**Desarrollo full stack**
Trabajo que comprende frontend, backend, base de datos, testing, seguridad, herramientas y despliegue.

### E

**Eloquent**
ORM de Laravel. Permite representar tablas mediante modelos PHP y construir consultas utilizando objetos y métodos.

**Environment (`.env`)**
Configuración específica de un entorno: conexión de base de datos, URL, modo debug y otras variables. `.env` puede contener secretos y no se publica en Git.

### F

**Factory**
Clase que genera datos de prueba para un modelo. Se usa habitualmente en tests y seeders.

**Fortify**
Paquete de Laravel que proporciona la lógica backend de autenticación, como login, registro, recuperación de contraseña y verificación de correo.

**Frontend**
Parte que se ejecuta en el navegador. En LaraCode incluye Vue, TypeScript, Inertia y Tailwind CSS.

### G

**Git**
Sistema de control de versiones distribuido. Registra cambios y permite trabajar con ramas, commits y fusiones.

**GitHub**
Servicio remoto para alojar repositorios Git, revisar cambios mediante Pull Requests y colaborar.

### H

**HTTP**
Protocolo usado por navegador y servidor para comunicarse. Una petición HTTP contiene método, URL, cabeceras y, en ocasiones, datos.

### I

**Inertia**
Capa que conecta Laravel con Vue. Laravel sigue controlando rutas y respuestas, mientras Vue renderiza las páginas sin necesitar una API separada.

**Indentación**
Espacios situados al comienzo de una línea para representar estructura y mejorar la lectura. No sustituye a llaves o etiquetas, pero hace visible su jerarquía.

### L

**Laravel**
Framework PHP principal de LaraCode. Proporciona rutas, middleware, validación, autenticación, Eloquent, tests y numerosos servicios.

**Layout**
Componente que define la estructura visual compartida por varias páginas, por ejemplo navegación, sidebar y zona de contenido.

### M

**Merge (fusión)**
Operación que integra los commits de una rama en otra.

**Middleware**
Capa que examina o modifica una petición antes de que llegue a su destino. `auth` y `verified` son ejemplos.

**Migration (migración)**
Archivo PHP versionado que describe cambios en la estructura de la base de datos.

**Model (modelo)**
Clase que representa y manipula datos de una tabla mediante Eloquent.

**Monolito**
Aplicación cuyo backend y frontend forman un único proyecto desplegable. LaraCode es un monolito Laravel con Inertia.

### N

**Node.js**
Entorno utilizado para ejecutar herramientas JavaScript fuera del navegador, como Vite, ESLint y TypeScript.

**npm**
Gestor de paquetes JavaScript. Lee `package.json` e instala dependencias dentro de `node_modules/`.

### O

**ORM (Object-Relational Mapper)**
Herramienta que conecta objetos del lenguaje con tablas relacionales. Eloquent es el ORM de Laravel.

### P

**Pest**
Framework de testing PHP utilizado por LaraCode. Ofrece una sintaxis expresiva sobre PHPUnit.

**PHP**
Lenguaje de programación utilizado en el backend de Laravel.

**Pint**
Formateador de código PHP de Laravel. Corrige automáticamente el estilo del código.

**Prop**
Dato que un componente Vue recibe desde su padre o, en una página de Inertia, desde la respuesta del servidor.

**Pull**
Operación Git que obtiene e integra cambios desde una rama remota.

**Pull Request (PR)**
Propuesta en GitHub para revisar y fusionar una rama en otra.

**Push**
Operación Git que publica commits locales en un repositorio remoto.

### R

**Request (petición)**
Mensaje enviado al servidor. Incluye qué recurso se solicita y mediante qué método HTTP.

**Response (respuesta)**
Mensaje que el servidor devuelve al cliente. Puede contener HTML, una respuesta Inertia, JSON, una redirección o un error.

**Route (ruta)**
Regla que relaciona un método y una URI con una acción. Ejemplo: `GET /dashboard`.

### S

**Seeder**
Clase que inserta datos iniciales o de demostración en la base de datos.

**Session (sesión)**
Mecanismo que permite recordar al usuario entre peticiones. Laravel la utiliza para mantener la autenticación.

**SPA (Single-Page Application)**
Aplicación que actualiza la página mediante JavaScript sin recargar completamente el documento en cada navegación. Inertia proporciona esta experiencia conservando rutas de servidor.

### T

**Tailwind CSS**
Framework CSS basado en clases utilitarias. Permite construir estilos directamente en el marcado.

**Test**
Código que ejecuta una comprobación automática sobre el comportamiento de la aplicación.

**TypeScript**
Extensión tipada de JavaScript. Ayuda a detectar errores antes de ejecutar el frontend.

### V

**VILT**
Acrónimo de Vue, Inertia, Laravel y Tailwind CSS.

**Vite**
Herramienta que sirve y compila los recursos del frontend.

**Vue**
Framework JavaScript utilizado para construir la interfaz de LaraCode mediante componentes reactivos.

### W

**Wayfinder**
Herramienta de Laravel que genera funciones TypeScript para utilizar rutas y acciones del backend desde el frontend de forma tipada.

---

## Guía para leer y escribir código

### 1. La indentación muestra jerarquía

Cada nivel interior utiliza cuatro espacios en este proyecto:

```php
Route::middleware(['auth'])->group(function () {
    Route::get('/example', function () {
        return 'Example';
    });
});
```

Una forma de leerlo es:

```text
grupo protegido
└── ruta /example
    └── respuesta Example
```

Si una línea está más desplazada a la derecha, pertenece visualmente al bloque anterior.

### 2. Las parejas que deben cerrarse

Al leer código, busca siempre su pareja:

| Apertura | Cierre   | Uso habitual                          |
| -------- | -------- | ------------------------------------- |
| `(`      | `)`      | Parámetros y condiciones              |
| `[`      | `]`      | Arrays                                |
| `{`      | `}`      | Bloques PHP/JavaScript y objetos      |
| `<div>`  | `</div>` | Elementos HTML/Vue                    |
| `'`      | `'`      | String con comillas simples           |
| `"`      | `"`      | String o atributo con comillas dobles |

Cuando aparezca un error de sintaxis, revisa primero si falta uno de estos cierres.

### 3. Cómo se compone una ruta Laravel

```php
Route::inertia('dashboard', 'Dashboard')->name('dashboard');
```

Se puede separar así:

```text
Route            clase/fachada utilizada
::               acceso a un método estático
inertia(...)     método llamado
'dashboard'      URI
'Dashboard'      página Vue solicitada
->               encadena otra llamada sobre el resultado
name(...)        asigna el nombre interno de la ruta
;                termina la instrucción PHP
```

Truco: lee una cadena de métodos de izquierda a derecha como una frase:

> Crea una ruta Inertia para `dashboard`, renderiza `Dashboard` y llámala `dashboard`.

### 4. Diferencia entre `::`, `->` y `=>`

```php
Route::get(...);      // :: accede a un miembro estático de una clase
$user->email;        // -> accede a un miembro de un objeto
'name' => 'Carlos';  // => relaciona clave y valor en un array
```

Aunque se parecen visualmente, representan operaciones distintas.

### 5. Anatomía de un componente Vue

```vue
<script setup lang="ts">
const title = 'Dashboard';
</script>

<template>
    <h1>{{ title }}</h1>
</template>
```

- `<script setup>` contiene comportamiento y datos.
- `lang="ts"` activa TypeScript.
- `<template>` describe lo que se renderiza.
- `{{ title }}` imprime una expresión en el template.
- El componente debe tener un único elemento raíz.

### 6. Atributos y directivas Vue

```vue
<Link v-if="user" :href="dashboard()" @click="trackVisit">
    Dashboard
</Link>
```

```text
v-if       renderiza según una condición
:href      enlaza el atributo a una expresión; equivale a v-bind:href
@click     escucha un evento; equivale a v-on:click
```

Sin `:`, el valor se interpreta como texto literal. Con `:`, Vue evalúa una expresión.

### 7. Imports y alias

```ts
import { dashboard } from '@/routes';
```

- `import` trae código de otro módulo.
- `{ dashboard }` importa un miembro concreto.
- `@/` es un alias que apunta a `resources/js/`.
- Wayfinder genera las funciones de `@/routes` a partir de rutas Laravel.

### 8. Convenciones de nombres

| Elemento        | Convención                    | Ejemplo                  |
| --------------- | ----------------------------- | ------------------------ |
| Clase PHP       | PascalCase                    | `CourseController`       |
| Componente Vue  | PascalCase                    | `CourseCard.vue`         |
| Variable/método | camelCase                     | `completedLessons`       |
| Tabla/columna   | snake_case                    | `lesson_attempts`        |
| Ruta con nombre | palabras separadas por puntos | `courses.show`           |
| Rama Git        | número y kebab-case inglés    | `003-trace-vilt-request` |

Un buen nombre explica intención. Evita abreviaturas como `$usr`, `$data2` o `doThing()`.

### 9. Comentarios: explica el porqué

Comentario poco útil:

```php
// Get the user.
$user = $request->user();
```

El código ya dice qué hace. Un comentario es útil cuando explica una decisión no evidente:

```php
// Keep the tests isolated from the developer's MySQL database.
```

Los comentarios de código de LaraCode se escriben en inglés.

### 10. Cómo leer código desconocido

Sigue este orden:

1. Identifica el archivo y su responsabilidad.
2. Revisa imports y namespace.
3. Busca la entrada principal: ruta, método, props o template.
4. Sigue una sola variable o petición cada vez.
5. Anota qué sabes y qué estás suponiendo.
6. Confirma las suposiciones ejecutando tests, inspeccionando rutas o usando el navegador.

No intentes comprender cada línea simultáneamente.

### 11. Cómo seguir una petición VILT

Utiliza esta lista:

```text
[ ] ¿Qué URL y método HTTP se utilizan?
[ ] ¿Qué ruta coincide?
[ ] ¿Qué middleware se ejecuta?
[ ] ¿Hay controlador o respuesta directa?
[ ] ¿Qué modelo o consulta interviene?
[ ] ¿Qué página Inertia se solicita?
[ ] ¿Qué props recibe?
[ ] ¿Qué componente Vue las renderiza?
[ ] ¿Qué ve finalmente el usuario?
```

### 12. Trucos de depuración

- Lee el primer error relevante, no solamente la última línea del stack trace.
- Comprueba el archivo y número de línea indicados.
- Si cambias PHP, revisa logs y tests.
- Si cambias Vue, revisa consola y panel de red del navegador.
- Si no aparece un cambio visual, comprueba `npm run dev` o ejecuta `npm run build`.
- Si Laravel no encuentra una ruta, utiliza `php artisan route:list`.
- Si la configuración parece antigua, ejecuta `php artisan config:clear`.
- Cambia una cosa cada vez para saber qué corrigió o provocó el problema.

---

## Términos pendientes de estudiar

Esta lista no significa que los conceptos estén aprendidos; indica vocabulario que añadiremos cuando aparezca de forma práctica:

- Authorization, Gate y Policy.
- Container e inyección de dependencias.
- Eager loading y problema N+1.
- Form Request.
- Queue y Job.
- Service Provider.
- Transacción de base de datos.
