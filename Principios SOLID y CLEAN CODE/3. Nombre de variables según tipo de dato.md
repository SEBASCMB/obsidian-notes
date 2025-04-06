
---

### Convenciones de Nomenclatura Específicas 🧐

Además de los principios generales, existen convenciones útiles para nombrar variables según el tipo de dato que contienen y para nombrar funciones, haciendo el código aún más predecible y fácil de seguir.

#### 1. Arreglos (Arrays) 📚

Cuando una variable contiene una colección de elementos (como un arreglo), su nombre debe reflejar esa pluralidad.

❌ **Mal:** (Nombre singular para una colección)

```javascript
// 'fruit' sugiere un solo elemento, no una lista.
const fruit = ['Manzana', 'Platano', 'Fresa'];
```

🤔 **Regular:** (Añade el tipo, pero puede ser redundante)

```javascript
// 'List' es explícito, pero 'fruits' (plural) suele ser suficiente.
const fruitList = ['Manzana', 'Platano', 'Fresa'];
```

✅ **Bueno:** (Usa el plural, la convención más común y clara)

```javascript
// 'fruits' indica claramente que es una colección de frutas.
const fruits = ['Manzana', 'Platano', 'Fresa'];
```

✨ **Mejor (Contextual):** (Más específico si es necesario)

```javascript
// Si el contexto lo requiere (ej. tienes 'fruitObjects' y 'fruitNames'),
// ser más específico puede mejorar la claridad.
const fruitNames = ['Manzana', 'Platano', 'Fresa'];
```

**Clave:** Usa **sustantivos en plural** para colecciones. 🍇🍇🍇

#### 2. Booleanos (Booleans) ✅ / ❌

Los nombres de variables booleanas deben sonar como una pregunta de sí/no o una afirmación clara de estado. Usar prefijos como `is`, `has`, `can`, `should` ayuda enormemente.

❌ **Mal:** (Nombres ambiguos, no sugieren un valor true/false)

```javascript
const open     = true; // ¿Abierto qué? ¿Es un comando o un estado?
const write    = true; // ¿Escribir? ¿Permiso para escribir?
const fruit    = true; // ¿Verdadero si es fruta? ¿Tiene fruta?
const active   = false; // ¿Activo? ¿Inactivo? (El valor `false` aquí lo hace más confuso)
const noValues = true; // Doble negación, confuso. ¿True significa que 'no hay valores'?
const notEmpty = true; // Negación. ¿True significa que 'no está vacío'?
```

✅ **Mejor:** (Nombres claros que indican un estado verdadero/falso)

```javascript
const isOpen      = true;  // Responde: ¿Está abierto? Sí.
const canWrite    = true;  // Responde: ¿Puede escribir? Sí.
const hasFruit    = true;  // Responde: ¿Tiene fruta? Sí.
const isActive    = false; // Responde: ¿Está activo? No. (Claro y directo)
const hasValues   = false; // Prefiere afirmaciones positivas. False significa 'no tiene valores'.
const isEmpty     = false; // Prefiere afirmaciones positivas. False significa 'no está vacío'.
```

**Clave:** Usa prefijos como `is`, `has`, `can`, `should` y prefiere afirmaciones positivas. 🚦

#### 3. Números (Numbers) 🔢

Para variables numéricas, el nombre debe indicar *qué* representa ese número. Un simple sustantivo puede ser insuficiente.

❌ **Mal:** (El nombre no da contexto al número)

```javascript
const fruits = 3; // ¿3 qué? ¿Máximo? ¿Mínimo? ¿Total?
const cars   = 10;  // ¿10 qué?
```

✅ **Mejor:** (El nombre añade contexto y significado al valor numérico)

```javascript
const maxAllowedFruits  = 3;    // Límite superior claro.
const minRequiredFruits = 1;   // Límite inferior claro.
const totalFruitsOnHand = 3;   // Describe la cantidad total actual.

const numberOfCars = 10;      // Indica una cuenta o cantidad.
const maxCarsInLot = 50;      // Indica una capacidad máxima.
```

**Clave:** Añade contexto al nombre (`max`, `min`, `total`, `count`, `numberOf`, `index`, `amount`, etc.). #️⃣

#### 4. Funciones (Functions) ▶️

Los nombres de las funciones deben ser **verbos o frases verbales** que indiquen claramente la *acción* que realizan. Evita incluir lógica condicional (`if...`) en el nombre; la función debe hacer una cosa, y la decisión de llamarla se toma fuera o al principio de la función.

❌ **Mal:** (Nombres que describen la condición, no solo la acción principal)

```javascript
createUserIfNotExist(); // La condición 'IfNotExist' está en el nombre.
updateUserIfNotEmpty(); // La condición 'IfNotEmpty' está en el nombre.
sendEmailIfFieldsValid(); // La condición 'IfFieldsValid' está en el nombre.
```

✅ **Mejor:** (Nombres centrados en la acción principal; la lógica condicional va dentro o antes)

```javascript
// La función crea un usuario. La lógica para verificar si existe
// debería estar DENTRO de la función o ANTES de llamarla.
createUser();

// La función actualiza un usuario. La lógica para verificar
// si hay datos para actualizar va dentro o antes.
updateUser();

// La función envía un email. La validación de campos
// se hace antes de llamar o al inicio de la función.
sendEmail();
```

**Clave:** Nombra funciones con **verbos de acción claros**. Mantén la lógica condicional separada del nombre. ¡Haz que el nombre describa la acción principal! 🚀

---

¡Estas convenciones específicas ayudan a que cualquiera pueda entender rápidamente el propósito de una variable o función con solo leer su nombre! 🎉