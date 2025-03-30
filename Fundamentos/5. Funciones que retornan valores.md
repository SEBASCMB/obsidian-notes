
## 🔄 Funciones que Devuelven Valores: ¡Calculando y Entregando Resultados! 🎁

Hemos visto funciones como `mostrarVariable` que realizan una **acción** (mostrar algo en consola). Pero, ¿qué pasa si queremos que una función **calcule** algo y nos **entregue el resultado** para que podamos usarlo después (guardarlo en otra variable, pasarlo a otra función, etc.)?

¡Aquí es donde entra la poderosa palabra clave `return`! ✨

---

### La Magia de `return` ✨

Cuando una función encuentra la instrucción `return`, ocurren dos cosas importantes:

1.  **¡Alto! 🛑:** La función **detiene su ejecución** inmediatamente en ese punto. Cualquier código *después* del `return` dentro de la misma función no se ejecutará.
2.  **¡Toma! 🎁:** La función **devuelve** (o "retorna") el valor que está justo a la derecha del `return`. Este valor "sale" de la función y puede ser capturado o utilizado donde sea que la función fue llamada.

---

### Ejemplo 1: Creando un Saludo Personalizado 👋

Imagina que no solo queremos mostrar un nombre, sino crear una frase completa con él.

**1. Definición de la Función con `return`:**

```javascript
// Esta función toma un nombre (paramNombre) y DEVUELVE un nuevo string
function crearSaludo(paramNombre) {
  // Calcula el nuevo string y lo devuelve con 'return'
  return paramNombre + " es tu nombre ¡Qué genial!";
}
```

**2. Usando el Valor Devuelto:**

Simplemente llamar a `crearSaludo(nombre)` no mostrará nada por sí solo. La función *calcula* el saludo, pero necesitamos hacer algo con el valor que *devuelve*.

```javascript
let nombre = "Sebastian";

// Llamamos a la función y GUARDAMOS el resultado en una NUEVA variable
let saludoGenerado = crearSaludo(nombre);

// Ahora sí, mostramos el contenido de la variable que recibió el resultado
console.log(saludoGenerado);
```

**Resultado en la consola:** 👇
```
Sebastian es tu nombre ¡Qué genial!
```

¡Excelente! La función `crearSaludo` no modificó `nombre`, sino que **usó su valor** para **construir y devolver** un resultado completamente nuevo.

---

### Ejemplo 2: Una Calculadora Simple: Suma ➕

Las funciones que devuelven valores son perfectas para realizar cálculos.

**1. Definición de la Función:**

```javascript
// Esta función toma DOS números y DEVUELVE su suma
function sumarNumeros(num1, num2) {
  let resultado = num1 + num2;
  return resultado; // Devuelve el valor calculado
  // console.log("Esto no se ejecuta porque está después del return");
}

// También se puede hacer más corto:
// function sumarNumeros(num1, num2) {
//   return num1 + num2;
// }
```

**2. Usando el Resultado de la Suma:**

Podemos usar el valor devuelto de muchas maneras:

```javascript
// 1. Directamente dentro de otra función (como console.log)
console.log("La suma de 5 y 3 es:", sumarNumeros(5, 3));

// 2. Guardándolo en una variable para usarlo después
let total = sumarNumeros(10, 20);
console.log("El total calculado es:", total);
console.log("El doble del total es:", total * 2);
```

**Resultado en la consola:** 👇
```
La suma de 5 y 3 es: 8
El total calculado es: 30
El doble del total es: 60
```

---

## 💡 ¿Por Qué es Tan Útil `return`?

Usar `return` nos permite crear funciones que son como **bloques de construcción** 🧱:

*   **Reutilizables:** Calculan algo específico que podemos necesitar en varios lugares.
*   **Componibles:** El resultado de una función puede ser la entrada para otra. (`console.log(sumarNumeros(5, 3))` es un ejemplo simple).
*   **Testeables:** Es mucho más fácil verificar que una función devuelve el valor correcto (lo veremos con las pruebas).
*   **Flexibles:** Decidimos qué hacer con el resultado (mostrarlo, guardarlo, enviarlo a otro lado...).

Al separar la **lógica del cálculo** (dentro de la función con `return`) de la **acción a realizar con el resultado** (fuera de la función), nuestro código se vuelve mucho más modular, claro y potente. 💪

[[6. Funciones void - Funciones return]]