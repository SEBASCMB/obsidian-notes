
## 🤔 Tomando Decisiones en Código: ¡Los Condicionales! 🚦

En la vida real, tomamos decisiones constantemente: "Ummm, tengo hambre... 🍕 ¿Qué hay en la nevera? 🤔 ¡Ah, pizza de ayer! ✅ Genial. Si no hubiera habido pizza... 🍋 quizás ese limón cortado no era la mejor opción."

¡Podemos representar exactamente este tipo de **toma de decisiones** en nuestro código usando **condicionales**! La estructura más común es el `if`/`else`.

---

### 🗺️ Visualizando Decisiones: Diagramas de Flujo (Concepto)

Antes de escribir el código, a veces es útil visualizar el flujo de decisiones. Los programadores a menudo usan **diagramas de flujo**. Imagina un mapa que muestra el camino que seguirá tu programa.

**Símbolos Básicos en un Diagrama de Flujo Simple:**

| Símbolo        | Forma        | Significado                                      | Ejemplo en Código (Concepto) |
| :------------- | :----------- | :----------------------------------------------- | :--------------------------- |
| **Inicio/Fin** |  овальный       | 🏁 Indica dónde empieza y termina el proceso.     | (Inicio/Fin del script/función) |
| **Proceso**    | ▭ Rectángulo | ⚙️ Una acción o cálculo a realizar.             | `let resultado = a + b;`     |
| **Entrada/Salida** | ▱ Paralelogramo | 📥 Recibir datos (leer) o 📤 mostrar datos (imprimir). | `prompt(...)`, `console.log(...)` |
| **Decisión**   | 💎 Rombo       | 🤔 Una pregunta (condición) con **dos** salidas: Sí (✅) o No (❌). | `if (condicion) {...}`       |
| **Flujo**      | → Flecha     |  เส้นทาง Indica la dirección del proceso.         | (La secuencia de ejecución) |
![[Pasted image 20250330133723.png]]

![[Pasted image 20250330133742.png]]

![[Pasted image 20250330133820.png]]

**¿Cómo funciona?** Sigues las flechas desde el **Inicio** 🏁. Cuando llegas a un **Rombo** (Decisión 💎), evalúas la condición. Si es **Sí** (✅), sigues la flecha correspondiente. Si es **No** (❌), sigues la otra flecha. Continúas hasta llegar al **Fin** 🏁.

---

### `if`/`else`: La Decisión en Código JavaScript

La estructura `if`/`else` traduce directamente el rombo del diagrama:

*   `if (condicion)`: **SI** la condición dentro de los paréntesis `()` es verdadera (`true`), ejecuta el bloque de código dentro de las llaves `{}` siguientes.
*   `else`: **DE LO CONTRARIO** (si la condición del `if` fue falsa (`false`)), ejecuta el bloque de código dentro de las llaves `{}` del `else`.

**Ejemplo con Números:**

```javascript
const variable1 = 1;
const variable2 = 2; // ¡Son números!

// Pregunta: ¿Son AMBOS variables de tipo 'number'?
if (typeof variable1 === 'number' && typeof variable2 === 'number') {
  // ✅ SÍ: Ejecuta esto
  console.log("✅ ¡Ambos son números! Aquí están:", variable1, variable2);
} else {
  // ❌ NO: Ejecuta esto
  console.log("❌ Ups, al menos uno no es un número.");
}
```

**Resultado en consola:** 👇
```
✅ ¡Ambos son números! Aquí están: 1 2
```
*(Nota: Usamos `typeof variable === 'number'` para verificar si una variable contiene un número primitivo en JavaScript).*

---

### 👤 Agrupando Datos Relacionados: ¡Objetos!

A veces, queremos representar algo más complejo que un simple número o texto. Imagina describir a una persona: tiene nombre, edad, quizás pasatiempos... Para agrupar estas **propiedades** relacionadas bajo un mismo "paraguas", usamos **Objetos**.

Los objetos se definen con llaves `{}` y contienen pares de `clave: valor`.

```javascript
// Creamos un objeto para representar a una persona
const persona = {
  nombre: "Sebastian", // propiedad 'nombre' con valor string
  edad: 29,           // propiedad 'edad' con valor number (¡corregido!)
  ciudad: "Metropolis"
};

// Podemos acceder a sus propiedades usando el punto (.)
console.log("Nombre:", persona.nombre); // Muestra "Sebastian"
console.log("Edad:", persona.edad);     // Muestra 29
console.log("Datos completos:", persona); // Muestra el objeto entero
```

---

### 🚦 Tomando Decisiones con Propiedades de Objetos

Ahora podemos usar condicionales para tomar decisiones basadas en los datos de un objeto. ¡Combinemos todo!

**Función para verificar la mayoría de edad:**

```javascript
// Función que recibe un objeto 'persona' y verifica su edad
function esMayorDeEdad(individuo) {
  // La condición AHORA accede a la propiedad 'edad' del objeto recibido
  if (individuo.edad >= 18) {
    return true; // Devuelve VERDADERO si la edad es 18 o más
  } else {
    return false; // Devuelve FALSO si la edad es menor a 18
  }
}

// --- ¡Un Atajo Inteligente! ---
// La comparación (individuo.edad >= 18) YA devuelve true o false.
// ¡Podemos retornar directamente ese resultado!
function esMayorDeEdadShortcut(individuo) {
  return individuo.edad >= 18; // Más corto y hace lo mismo 👍
}

// --- Probando las funciones ---
const alan = { nombre: "Alan", edad: 17 };
const maria = { nombre: "Maria", edad: 35 };

console.log(persona.nombre + " ¿es mayor de edad? (v1)", esMayorDeEdad(persona));          // Usa Sebastian (29) -> true
console.log(alan.nombre + " ¿es mayor de edad? (v1)", esMayorDeEdad(alan));                // Usa Alan (17) -> false

console.log(maria.nombre + " ¿es mayor de edad? (shortcut)", esMayorDeEdadShortcut(maria)); // Usa Maria (35) -> true
```

**Resultado en consola:** 👇
```
Nombre: Sebastian
Edad: 29
Datos completos: { nombre: 'Sebastian', edad: 29, ciudad: 'Metropolis' }
Sebastian ¿es mayor de edad? (v1) true
Alan ¿es mayor de edad? (v1) false
Maria ¿es mayor de edad? (shortcut) true
```

---

### ✨ El Operador Ternario: `condicion ? valorSiTrue : valorSiFalse`

Para condicionales simples donde queremos **asignar un valor** a una variable dependiendo de una condición, existe una sintaxis más corta y elegante: el **operador ternario**.

```javascript
let edadUsuario = 20;

// Forma larga con if/else
let mensajeEdad;
if (edadUsuario >= 18) {
  mensajeEdad = "Es mayor de edad";
} else {
  mensajeEdad = "Es menor de edad";
}
console.log("(if/else) Mensaje:", mensajeEdad);

// Forma corta con Operador Ternario
let mensajeEdadTernario = (edadUsuario >= 18) ? "Es mayor de edad" : "Es menor de edad";
//                      (      condición      ) ? ( valor si TRUE ) : ( valor si FALSE )
console.log("(Ternario) Mensaje:", mensajeEdadTernario);

// Aplicado a nuestro objeto 'persona'
const miResultado = persona.edad >= 18 ? "✅ Sí, puede pasar." : "❌ No, muy joven.";
console.log("¿Puede pasar Sebastian?", miResultado);
```

**Resultado en consola:** 👇
```
(if/else) Mensaje: Es mayor de edad
(Ternario) Mensaje: Es mayor de edad
¿Puede pasar Sebastian? ✅ Sí, puede pasar.
```

¡El operador ternario es genial para asignaciones condicionales rápidas!

---

Los condicionales (`if`/`else` y ternarios) son fundamentales en programación. ¡Nos permiten crear lógica, responder a diferentes situaciones y hacer que nuestros programas sean mucho más inteligentes y flexibles! 🧠💡

[[8. Loops]]