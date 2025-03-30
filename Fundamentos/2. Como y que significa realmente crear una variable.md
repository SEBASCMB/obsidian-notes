
# 📦 Variables en JavaScript: ¡Guardando Información! 🏷️

Cuando programamos, necesitamos una forma de **guardar** y **recordar** información para usarla más tarde. ¡Ahí es donde entran las **variables**! Piensa en ellas como **cajas con etiquetas** donde podemos almacenar datos.

---

## ✍️ Creando Nuestra Primera Variable

Imagina que queremos guardar tu nombre. Usamos una palabra clave (`let` o `const` son las más modernas, `var` es más antiguo), le damos un **nombre** (la etiqueta de la caja) y le **asignamos** un valor (lo que va dentro de la caja) usando `=`.

```javascript
// Usamos 'let' porque el valor podría cambiar (aunque no lo haremos aquí)
let nombre = "Sebastian"; // Creamos la variable 'nombre' y guardamos el texto "Sebastian"
```

*   `let`: Palabra clave para declarar la variable.
*   `nombre`: El identificador o nombre que le damos (¡nuestra etiqueta!).
*   `=`: El operador de asignación (mete el valor en la caja).
*   `"Sebastian"`: El valor que estamos guardando (en este caso, un texto o *string*).

---

## 👀 Mirando Dentro de la Caja: `console.log()`

Si queremos saber qué hay guardado dentro de nuestra variable `nombre`, podemos pedirle a JavaScript que lo muestre en la **consola** (una herramienta fundamental para desarrolladores).

```javascript
console.log(nombre); // Le decimos: "Muestra en consola el valor de la variable 'nombre'"
```

**Resultado en la consola:** 👇
```
Sebastian
```

---

## 🤔 ¿Qué Pasa "Debajo del Capó"? ¡La Memoria! 🧠💾

Esta parte es **crucial** para entender cómo funcionan las cosas:

Cuando hacemos `let nombre = "Sebastian";`, le estamos diciendo a la computadora:

1.  **"Reserva un pequeño espacio en tu memoria RAM."** 💻
2.  **"Etiqueta ese espacio con la palabra `nombre`."** 🏷️ (Este `nombre` es una **referencia** a esa ubicación de memoria).
3.  **"Guarda el valor `"Sebastian"` dentro de ese espacio etiquetado."** 📄

Así, cada vez que usamos `nombre` en nuestro código, la computadora sabe que tiene que ir a buscar el valor guardado en ese lugar específico de la memoria que etiquetamos.

✨ ¡Entender que la variable es una **referencia** a un valor en **memoria** es un concepto súper importante en programación! ✨

---

## 🗂️ ¡No Todas las Cajas Son Iguales! Tipos de Variables

Podemos guardar diferentes **tipos** de información. JavaScript es flexible, pero es bueno saber qué tipo de dato estamos manejando:

```javascript
// Tipo: String (Texto) 📝
// Se usan comillas simples ('') o dobles ("")
let miNombre = 'Sebastian';
let saludo = "¡Hola Mundo!";

// Tipo: Number (Número) 🔢
// Pueden ser enteros o decimales
let edad = 30;
let precio = 99.95;
let temperatura = -5;

// Tipo: Boolean (Booleano) ✅❌
// Solo puede ser verdadero (true) o falso (false)
let esMayorDeEdad = true;
let tieneDescuento = false;
```

---

## 📋 Agrupando Información: ¡Listas o Arrays!

A veces queremos guardar una **colección** de elementos relacionados, como una lista de nombres. Para eso usamos los **Arrays** (arreglos), que se definen con corchetes `[]`.

```javascript
// Creamos un array (lista) de strings (nombres)
let conjuntoDeNombres = ['Alan', 'Facu', 'Sebastian', 'Maria'];

console.log(conjuntoDeNombres); // Muestra toda la lista
```

**Resultado en la consola:** 👇
```
[ 'Alan', 'Facu', 'Sebastian', 'Maria' ]
```

A esto se le llama un **Array de Strings**, porque cada elemento dentro de la lista es un texto (string). ¡Podríamos tener arrays de números, booleanos, o incluso una mezcla!

---

[[3. Arreglos-Arrays]]