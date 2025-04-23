
## 🚀 Funciones en JavaScript: ¡Bloques de Código con Propósito! 🛠️

Hemos visto que las funciones son como **mini-recetas** o **instrucciones empaquetadas**. Ahora, profundicemos en sus dos "sabores" principales según su propósito: las que **realizan acciones** y las que **calculan y devuelven resultados**.

---

### 1. Funciones que Realizan Acciones (Efectos Secundarios) 💥

Algunas funciones tienen como objetivo principal **hacer algo**, provocar un cambio o interactuar con el "mundo exterior" de la función. A esto se le llama **efecto secundario**.

*   **Ejemplos de acciones:**
    *   Mostrar un mensaje en la consola (`console.log()`).
    *   Modificar un elemento en una página web (cambiar texto, estilo, etc.).
    *   Guardar datos en el almacenamiento local del navegador.
    *   Enviar información a un servidor.
    *   Cambiar el valor de una variable *fuera* de la función (variables globales - ¡cuidado con esto!).

Estas funciones **no están diseñadas primordialmente para devolver un valor calculado**.

```javascript
function saludarEnConsola(nombre) {
  // La acción principal es MOSTRAR algo
  console.log("¡Hola, " + nombre + "!");
  // No hay un 'return' con un valor específico
}

// Llamamos a la función por su ACCIÓN
saludarEnConsola("Mundo"); // Consola: ¡Hola, Mundo!

// ¿Qué pasa si intentamos guardar lo que "devuelve"?
let resultadoSaludo = saludarEnConsola("Ana");
console.log("Resultado guardado:", resultadoSaludo);
```

**Resultado en la consola:** 👇
```
¡Hola, Mundo!
¡Hola, Ana!
Resultado guardado: undefined
```

**Importante:** En JavaScript, si una función no tiene una instrucción `return <valor>` explícita (o solo `return;`), **técnicamente devuelve `undefined`**. Aunque devuelvan `undefined`, su valor real está en la *acción* que realizan. En otros lenguajes (como C++, Java, C#), este tipo de funciones se declararían explícitamente como `void`.

---

### 2. Funciones que Devuelven Valores Calculados 🎁 (`return`)

Estas son las funciones que actúan como **bloques de construcción** 🧱. Su propósito principal es **calcular un resultado** basado en sus entradas (parámetros) y **entregarlo** usando la palabra clave `return`.

**La Magia de `return` ✨:**

Cuando una función encuentra `return <valor>`:
1.  **¡Alto! 🛑:** Detiene su ejecución.
2.  **¡Toma! 🎁:** Devuelve el `<valor>` especificado, permitiéndonos capturarlo y usarlo.

**Ejemplo: Creando un Saludo Personalizado (Revisado)** 👋

```javascript
// Esta función CALCULA y DEVUELVE un string
function crearSaludoCompleto(paramNombre) {
  return paramNombre + " es tu nombre ¡Qué genial!"; // Devuelve el resultado
}

let nombreUsuario = "Carlos";
// CAPTURAMOS el valor devuelto en una variable
let saludoParaCarlos = crearSaludoCompleto(nombreUsuario);

// USAMOS el valor capturado
console.log(saludoParaCarlos); // Consola: Carlos es tu nombre ¡Qué genial!
```

**Ejemplo: Calculadora Simple: Suma (Revisado)** ➕

```javascript
// Esta función CALCULA y DEVUELVE la suma
function sumarNumeros(num1, num2) {
  return num1 + num2; // Devuelve la suma
}

// USAMOS el valor devuelto directamente
console.log("Resultado directo:", sumarNumeros(15, 7)); // Consola: Resultado directo: 22

// O lo guardamos para usarlo más tarde
let sumaImportante = sumarNumeros(100, 200);
console.log("Suma guardada:", sumaImportante); // Consola: Suma guardada: 300
```

---

### 💡 Patrones Comunes de Funciones que Retornan Valores

Las funciones que devuelven valores son increíblemente versátiles. Aquí algunos tipos comunes según lo que retornan:

*   **Boolean (`true`/`false`) ✅❌:** Para comprobaciones y decisiones.
    *   `function esMayorDeEdad(edad) { return edad >= 18; }`
    *   `function estaVacio(array) { return array.length === 0; }`
    *   `function tienePermisos(usuario) { /* lógica compleja */; return true; /* o false */ }`

*   **Number (Números) 🔢:** Para cálculos matemáticos o conteos.
    *   `function calcularAreaCirculo(radio) { return Math.PI * radio * radio; }`
    *   `function obtenerPromedio(numeros) { /*...*/ }`
    *   `function contarVocales(texto) { /*...*/ }`

*   **String (Texto) 📝:** Para formatear, generar o extraer texto.
    *   `function formatearFecha(fecha) { /*...*/ }`
    *   `function generarMensajeError(codigo) { /*...*/ }`
    *   `function obtenerIniciales(nombreCompleto) { /*...*/ }`

*   **Array (Listas) 📋:** Para filtrar, transformar o agrupar colecciones de datos.
    *   `function obtenerUsuariosActivos(listaUsuarios) { /*...*/ }`
    *   `function convertirCsvAArray(textoCsv) { /*...*/ }`
    *   `function obtenerNombres(listaObjetos) { /*...*/ }`

*   **Object (Objetos) 🧩:** Para crear, buscar o configurar estructuras de datos complejas.
    *   `function obtenerDatosUsuario(idUsuario) { /* busca en BD o API */; return { id: id, nombre: '...', email: '...' }; }`
    *   `function crearConfiguracionDefault() { return { tema: 'oscuro', notificaciones: true }; }`
    *   `function parsearJson(textoJson) { return JSON.parse(textoJson); }`

---

## ✅ Conclusión: ¿Acción o Resultado?

Entender la diferencia es clave:

*   Llama a una función por su **acción** si su objetivo principal es un **efecto secundario** (como `console.log`). No esperes un valor útil de retorno (será `undefined` si no hay `return`).
*   Llama a una función y **usa su `return`** si su objetivo es **calcular y entregar un valor**. Captura ese valor en una variable o úsalo directamente.

Separar la lógica de cálculo (`return`) de las acciones (efectos secundarios) hace tu código más predecible, modular, fácil de probar y reutilizable. ¡Piensa en funciones como herramientas especializadas en tu caja de desarrollo! 🔧🧠

[[7. Condicionales]]