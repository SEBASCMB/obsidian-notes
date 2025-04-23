# Variables en JavaScript

Las variables son contenedores de información que apuntan a un lugar en la memoria de la computadora. Se utilizan para almacenar y manipular datos en un programa, permitiendo acceder a estos valores mediante un nombre de referencia.

## Tipos de declaración de variables

### 1. let

Declara una variable que puede ser modificada posteriormente. Su alcance está limitado al bloque donde se declara.

**Ejemplo:**

```javascript
let edad = 25; // Declaración inicial
edad = 26;     // Valor modificado

if (true) {
  let mensaje = "Hola"; // Solo existe dentro de este bloque
}
// console.log(mensaje); // Error: mensaje no está definido fuera del bloque
```

### 2. const

Declara una variable con valor inmutable. Una vez asignado un valor, no puede ser reasignado.

**Ejemplo:**

```javascript
const PI = 3.14159;
// PI = 3.14; // Error: no se puede reasignar una constante

// Sin embargo, si es un objeto o array, sus propiedades pueden modificarse
const persona = { nombre: "Ana" };
persona.nombre = "Carlos"; // Esto es válido
// persona = { nombre: "Carlos" }; // Error: no se puede reasignar la constante
```

### 3. var (deprecado)

Forma tradicional de declarar variables, con alcance de función en lugar de bloque. Actualmente no se recomienda su uso.

**Ejemplo:**

```javascript
var contador = 1;
contador = 2; // Puede modificarse

if (true) {
  var global = "Visible fuera del bloque"; // Alcance de función, no de bloque
}
console.log(global); // Funciona, "Visible fuera del bloque"
```

## Reglas de nombrado

- Los nombres deben comenzar con letra, guion bajo (_) o signo de dólar ($)
- Pueden contener letras, números, guiones bajos y signos de dólar
- Son sensibles a mayúsculas y minúsculas (`miVariable` es diferente de `MiVariable`)
- No pueden ser palabras reservadas (como `if`, `function`, `return`, etc.)

## Convenciones de nombrado

```javascript
// camelCase (recomendado para variables y funciones)
let nombreCompleto = "Juan Pérez";

// PascalCase (usado para clases y constructores)
class Usuario {}

// snake_case
let nombre_usuario = "admin";

// SCREAMING_SNAKE_CASE (para constantes importantes)
const MAX_INTENTOS = 3;
```

## Ámbito de las variables

- **Ámbito global**: Variables declaradas fuera de cualquier función o bloque
- **Ámbito de función**: Variables declaradas dentro de una función
- **Ámbito de bloque**: Variables declaradas con `let` o `const` dentro de un bloque `{}`

## Buenas prácticas

- Usar `const` por defecto, y `let` solo cuando necesites reasignar valores
- Evitar el uso de `var`
- Elegir nombres descriptivos que expliquen el propósito de la variable
- Declarar las variables al inicio de su ámbito
- Inicializar las variables al declararlas cuando sea posible

## Tipos de datos que pueden almacenar

```javascript
let texto = "Hola mundo";        // String
let numero = 42;                 // Number
let esVerdadero = true;          // Boolean
let noDefinido;                  // undefined
let nulo = null;                 // null
let objeto = { clave: "valor" }; // Object
let arreglo = [1, 2, 3];         // Array (tipo de objeto)
let funcion = function() {};     // Function (tipo de objeto)
```