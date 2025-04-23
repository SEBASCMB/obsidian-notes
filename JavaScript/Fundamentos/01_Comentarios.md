# Comentarios en JavaScript

Los comentarios en JavaScript son líneas de código que el intérprete ignora al ejecutar el programa. Son útiles para:

- Explicar el propósito del código
- Documentar funcionalidades
- Des habilitar temporalmente código sin eliminarlo
- Facilitar el mantenimiento del código
- Mejorar la colaboración entre desarrolladores

## Tipos de comentarios

### 1. Comentarios de una sola línea

Se crean utilizando dos barras diagonales (`//`). Todo lo que sigue en esa línea será ignorado por el intérprete.

**Ejemplo:**

```javascript
// Este es un comentario de una sola línea
console.log("Este código sí se ejecutará");

let nombre = "María"; // También puedes añadir comentarios al final de una línea de código
```

### 2. Comentarios multilínea

Se crean utilizando `/*` para abrir y `*/` para cerrar. Todo lo que esté entre estos símbolos será ignorado, incluso si abarca múltiples líneas.

**Ejemplo:**

```javascript
/* Este es un comentario
   que ocupa varias líneas
   y todo será ignorado por el intérprete */

/* También puedes usar comentarios multilínea
   para documentar funciones complejas */
function calcularImpuestos(monto) {
    return monto * 0.16;
}
```

### 3. Comentarios de documentación (JSDoc)

Son un tipo especial de comentarios multilínea que siguen una sintaxis específica para generar documentación automática.

**Ejemplo:**

```javascript
/**
 * Calcula el área de un círculo
 * @param {number} radio - El radio del círculo
 * @returns {number} El área del círculo
 */
function calcularAreaCirculo(radio) {
    return Math.PI * radio * radio;
}
```

## Buenas prácticas

- Usa comentarios para explicar "por qué" se hace algo, no solo "qué" se hace
- Mantén los comentarios actualizados cuando cambies el código
- Evita comentarios obvios que no aportan información útil
- Usa comentarios para marcar secciones importantes o TODOs
- No abuses de los comentarios; el código debe ser auto explicativo cuando sea posible

## Casos de uso comunes

### Deshabilitar código temporalmente

```javascript
// console.log("Este mensaje de depuración no se mostrará");
// alert("Esta alerta está desactivada durante el desarrollo");
```

### Marcar tareas pendientes

```javascript
// TODO: Implementar validación de datos
// FIXME: Corregir problema con decimales
```

### Explicar algoritmos complejos

```javascript
/* 
 * Algoritmo de ordenación rápida (QuickSort)
 * Complejidad promedio: O(n log n)
 * Funcionamiento: Divide y vencerás...
 */
```