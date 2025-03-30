## Concatenación de Cadenas en Java
### **¿Que es la concatenación de cadenas?**

La **concatenación de cadenas** es el proceso de unir dos o mas cadenas para formar una nueva cadena. En java, existen varios métodos para concatenar cadenas, cada uno con sus propias características y usos.

**Métodos de Concatenación en Java**

1. **Operador +**
2. **Método `concat()`**
3. **Clase `StringBuilder`**
4. **Clase `StringBuffer`**
5. **Método `String.join()`**

### Operador +
El operador + es el metodo mas sencillo y comun para concatenar cadenas en Java. Es facil de usar y leer.

**Sintaxis:**
`String resultado = cadena1 + cadena2;`

**Ejemplo:**

```java
public class ConcatenacionOperador {

	publiic static void main(String[] args) {
	
		String saludo = "Hola";
		String nombre = "Sebastian";
		String mensaje = saludo " " + nombre + " ";

		System.out.println(mensaje);
	
	}

}
```

### Método concat()

Le método concact() de la clase String concatena la cadena especificada al final de la cadena actual.

**Sintaxis**
`String resultado = cadena1.concat(cadena2);`

**Ejemplo**

```java
public class ConcatenacionConcat {

	public static void main(String[] args){
	
		var saludo  = "Hola";
		var nombre  = "Sebastian"
		var mensaje = saludo.concat(" ").concat(nombre).concat("!");
		System.out.println(mensaje);
	
	}

}
```

### Clase StringBuilder

StringBuilder es mas eficiente para concatenaciones repetitivas y en bucles, ya que es mutable y no crea nuevas instancias de cadena

**Sintaxis:**

```java
var sb = new StringBuilder();
sb.append(cadena1);
sb.append(cadena2);
var resultado = sb.toString();
```

**Ejemplo:**

```java
public class ContenacionStringBuilder {

	public static void main(String[] args) {

		var saludo = "Hola";
		var nombre = "Mundo";
		var sb = new StringBuilder();
		sb.append(saludo);
		sb.append(" ");
		sb.append(nombre);
		sb.append("!");

		String mensaje = sb.toString();
		System.out.println(mensaje);

	}

}
```

### Clase StringBuffer

StringBuffer es similar StringBuilder. pero es seguro para hilos (thread-safe), lo que lo hace adecuado para entornos multihilo.

**Sintaxis:**

```java
var sb. = new StringBuffer();
sb.append(cadena1);
sb.append(cadena2);
var resultado = sb.toString();
```

**Ejemplo:**

```java
public class ConcatenacionStringBuffer {

	public static void main(String[] args) {

		var saludo = "Hola";
		var nombre = "Sebastian"
		var sb     = new StringBuffer();
		sb.append(saludo);
		sb.append(" ");
		sb.append(nombre);
		sb.append("!");
		var mensaje = sb.toString();
		System.out.println(mensaje);

	}

}
```

### Metodo String.join()

String.join es útil cuando se necesita unir una colección de cadena con un delimitador.

**Sintaxis:**

var resultado = String.join(delimitador, cadena1, cadena2);

**Ejemplo:**

```java
public class ConcatenacionJoin {

	public static void main(String[] args) {

		var saludo  = "Hola";
		var nombre  = "Sebastian";
		var mensaje = String.join(" ", saludo, nombre) + "!";
		System.out.println(mensaje);
	
	}

}
```

### Conclusión

La concatenación de cadena es una operación común en Java y es importante conocer las diferentes formas de realizara y cuando usar cada meto. + y concat() son sencillos y legibles, mientras que StringBuilder y StringBuffer son mas eficientes para operaciones repetitivas, String.join() es útil para unir colecciones de cadenas con un delimitador