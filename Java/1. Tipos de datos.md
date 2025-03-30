Los tipos de datos en Java son una categorización de las variables que se utiliza en el lenguaje de programación. estas caracterizaciones determinan que tipo de valores pueden almacenarse en las variables y como se pueden manipular estos valores. Java es un lenguaje de programación fuertemente tipado, lo que significa que cada variable se declara con un tipo especifico

Java tiene dos categorías principales de tipos de datos:

1. Tipos de Datos Primitivos
2. Tipos de Datos de Referencia

- Tipos de Datos Primitivos

Java tiene 8 tipos de datos primitivos. Son los tipos de datos mas básicos y no derivan de ningún otro tipo


| Tipo de dato | Tamaño (bits)          | Rango de valores                                          | Descripcion                                                                  |
| ------------ | ---------------------- | --------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Byte         | 8                      | -128 a 127                                                | Un entero de 8 bits con signo                                                |
| short        | 16                     | -32,768 a 32,767                                          | Un entero de 16 bits con signo                                               |
| Int          | 32                     | -2,147,483,648 a 2,147,483,647                            | Un entero de 32 bits con signo                                               |
| long         | 64                     | -9,223,372,036,854,775,808 a<br>9,223,372,036,854,775,807 | Un entero de 64 bits con signo                                               |
| float        | 32                     | 3.40282347 x 10^38 (positivo y<br>negativo)               | Un numero en coma flotante de precision simple de 32 bits, sigue la IEEE 754 |
| double       | 64                     | 1.79769313486231570 x 10^308<br>(positivo y negativo)     | Un numero en coma flotante de precision doble de 64 bits, sigue la IEEE 754. |
| char         | 16                     | '\u0000' a '\uffff'                                       | Un caracter Unicode de 16 bits                                               |
| boolean      | 1 (tamaño no definido) | tureo o false                                             | representa un valor booleanos                                                |

```java
public class TiposPrimitivos {
	public class static void main(String[] args) {
	
		// Enteros
		byte unByte   = 127;
		short unShort = 32000;
		int unInt     = 2147483647;
		long unLong   = 9223372036854775807L;

		// Punto flotante
		float unFloat   = 3.14f;
		double unDouble = 3.141592653589793;

		// Caracter
		char unChar = 'A';

		// Booleano
		boolean unBoolean = true;

		// Imprimir valores
		System.out.println("byte: " + unByte);
		System.out.println("short: " + unShort);
		System.out.println("int: " + unInt);
		System.out.println("long: " + unLong);
		System.out.println("float: " + unFloat);
		System.out.println("double: " + unDouble);
		System.out.println("char: " + unChar);
		System.out.println("boolean: " + unBoolean);
		
	}
}
```

- **Tipos de Datos de Referencia (Tipos Object)**

Los tipos de datos de referencia en Java incluyen:

- **Clases** Definen objetos y sus métodos
- **Interfaces** Definen métodos que pueden ser implementados por las clases,
- **Arreglos** Colecciones de elementos del mismo tipo.

Los tipos de referencia los vamos a ver a detalles en el tema de clases y objetos

**Valores por Defecto**

Los valores por defecto son los valores asignados a la variables si no se inicializan explicita mente.

- **Primitivos:**
		- Byte, short, int, long: 0
		- float, double: 0.0
		- char: '\u0000'
		- boolean: false
- **Referencia:**
		- null

**Conceptos Clave**

1. **Variables primitivas:** Contienen valores simples y directos.
2. **Variables de Referencia:** Contienen referencias (punteros) a objetos

## Usando Clases para Conocer Más Detalles de los Tipos Primitivos en Java

En Java, puedes utilizar clases envolventes (wrapper classes) para obtener más detalles y
funcionalidad adicional para los tipos de datos primitivos. Las clases envolventes
proporcionan métodos útiles y permiten trabajar con tipos primitivos como si fueran
objetos.

### **Clases Envolventes**
Para cada tipo de dato primitivo, existe una clase envolvente correspondiente en el paquete
java.lang. Estas clases permiten tratar los valores primitivos como objetos y proporcionan
métodos para convertir y manipular datos.


| Tipo Primitivo | Clase Envolvente |
| -------------- | ---------------- |
| byte           | Byte             |
| short          | Short            |
| int            | Integer          |
| long           | Long             |
| float          | Float            |
| double         | Double           |
| char           | Character        |
| boolean        | Boolean          |

### Ejemplos y Métodos Útiles

1. **Integer (para int)**

La clase ==Integer== proporciona métodos para trabajar con valores enteros.

**Métodos útiles:**

- `Ìnteger.parseInt(String s):` Convierte una cadena a un entero.
- `Ìnteger.toString(int i):` Convierte un entero a una cadena.
- `Integer.MAX_VALUE:` Valor máximo de un int
- `Integer.MIN_VALUE:` Valor mínimo de un int

#### Ejemplos
```java
public class DetallesInteger {

    public static void main(String[] args) {

        int number = 42;

        // Convetir a cadena
        String numberStr = Integer.toString(number);
        System.out.printf("Numero a cadena: %s%n", numberStr);

        // Valor maximo y minimo
        System.out.println("Valor maximo de int: " + Integer.MAX_VALUE);
        System.out.println("Valor minimo de int: " + Integer.MIN_VALUE);

        // Parsear de cadena a entero
        int parsedNumber = Integer.parseInt("123");
        System.out.println("Cadena a numero: " + parsedNumber);

        // Parsear de cadena a entero con formato
        int parsedNumberWithFormat = Integer.parseInt("123", 10);
        System.out.println("Cadena a numero con formato: " + parsedNumberWithFormat);

        // Parsear de cadena a entero con formato hexadecimal
        int parsedNumberWithHexFormat = Integer.parseInt("123", 16);
        System.out.println("Cadena a numero con formato hexadecimal: " + parsedNumberWithHexFormat);

        // Parsear de cadena a entero con formato octal
        int parsedNumberWithOctalFormat = Integer.parseInt("123", 8);
        System.out.println("Cadena a numero con formato octal: " + parsedNumberWithOctalFormat);

        // Parsear de cadena a entero con formato binario
        int parsedNumberWithBinaryFormat = Integer.parseInt("101010", 2);
        System.out.println("Cadena a numero con formato binario: " + parsedNumberWithBinaryFormat);

    }

}
```

2. **Double (para double)**

La clase `Double` proporciona métodos para trabajar con valores de punto flotante

**Métodos útiles:**

- `Double.parseDouble(String s)` Convierte una cadena a un double
- `Double.toString(double d)` Convierte un double a una cadena
- `Double.MAX_VALUE:` Valor máximo de un double
- `Double.MIN_VALUE:` Valor mínimo de un double

```java
public class DetalleDouble {

	public static void main(String[] args) {

		double numero = 3.14159;

		// Convertir a cadena
		String numeroStr = Double.toString(numero)
		System.out.println("Numero como candea: " + numero);

		// Valor maximo y Valor minimo
		System.out.println("Valor maximo de un double: " +    Double.MAX_VALUE);
		System.out.println("Valor minimo de un double: " + Double.MIN_VALUE);

		// Parsear cadena a double
		double parsedNumero = Double.parseDouble("2.71828");
		System.out.println("Numero parseado: " + parsedNumero);

	}

}
```