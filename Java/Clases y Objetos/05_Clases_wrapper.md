Las classes wrapper son clases que envuelven los tipos de datos primitivos para transformarlos en objetos es decir en clases y esto claramento tiene una ventaja

Integer
Double
Boolean
Character
Float

```java
package Integers;

public class WrapperInteger {

    public static void main(String[] args) {
        // Ejemplos con Integer
        int number = Integer.parseInt("123"); // número = 123
        System.out.println("El valor de 'number' es: " + number);

        Integer wrapper = Integer.valueOf("123"); // wrapper = 123 (como Integer)
        System.out.println("El valor de 'wrapper' es: " + wrapper);

        String text = Integer.toString(123); // texto = "123"
        System.out.println("El valor de 'text' es: " + text);

        int result = Integer.compare(10, 20); // resultado = -1 (porque 10 < 20)
        System.out.println("El resultado de 'Integer.compare(10, 20)' es: " + result);

        int max = Integer.max(10, 20); // max = 20
        System.out.println("El valor de 'max' es: " + max);

        int min = Integer.min(10, 20); // min = 10
        System.out.println("El valor de 'min' es: " + min);

        // Ejemplos con Byte
        byte number2 = Byte.parseByte("127"); // número = 127
        System.out.println("El valor de 'number2' es: " + number2);

        Byte wrapper2 = Byte.valueOf("127"); // wrapper = 127 (como Byte)
        System.out.println("El valor de 'wrapper2' es: " + wrapper2);

        String text2 = Byte.toString((byte) 127); // texto = "127"
        System.out.println("El valor de 'text2' es: " + text2);

        // Ejemplos con Short
        short number3 = Short.parseShort("32000"); // número = 32000
        System.out.println("El valor de 'number3' es: " + number3);

        Short wrapper3 = Short.valueOf("32000"); // wrapper = 32000 (como Short)
        System.out.println("El valor de 'wrapper3' es: " + wrapper3);

        String text3 = Short.toString((short) 32000); // texto = "32000"
        System.out.println("El valor de 'text3' es: " + text3);

        // Ejemplos con Long
        long number4 = Long.parseLong("123456789"); // número = 123456789
        System.out.println("El valor de 'number4' es: " + number4);

        Long wrapper4 = Long.valueOf("123456789"); // wrapper = 123456789 (como Long)
        System.out.println("El valor de 'wrapper4' es: " + wrapper4);

        String text4 = Long.toString(123456789L); // texto = "123456789"
        System.out.println("El valor de 'text4' es: " + text4);
    }

}
```

```java
package Doubles;

public class WrapperDoubleFloat {
    public static void main(String[] args) {
        // Ejemplos con Double
        double number = Double.parseDouble("3.14"); // número = 3.14
        System.out.println("El valor de 'number' es: " + number);

        Double wrapper = Double.valueOf("3.14"); // wrapper = 3.14 (como Double)
        System.out.println("El valor de 'wrapper' es: " + wrapper);

        int result = Double.compare(3.14, 2.71); // resultado = 1 (porque 3.14 > 2.71)
        System.out.println("El resultado de 'Double.compare(3.14, 2.71)' es: " + result);

        String text = Double.toString(3.24f); // texto = "3.24"
        System.out.println("El valor de 'text' es: " + text);



        // Ejemplos con Float
        float number2 = Float.parseFloat("3.14"); // número = 3.14
        System.out.println("El valor de 'number2' es: " + number2);

        Float wrapper3 = Float.valueOf("3.14"); // wrapper = 3.14 (como Float)
        System.out.println("El valor de 'wrapper3' es: " + wrapper3);

        String text2 = Float.toString(3.14f); // texto = "3.14"
        System.out.println("El valor de 'text2' es: " + text2);
    }

}
```

```java
package Characters;

public class WrapperCharacter {
    public static void main(String[] args) {
        boolean isLetter = Character.isLetter('A'); // esLetra = true
        boolean isDigit = Character.isDigit('5'); // esDigito = true
        boolean isWhiteSpace = Character.isWhitespace(' '); // esEspacio = true
        char upperText = Character.toUpperCase('a'); // mayuscula = 'A'
        char lowerText = Character.toLowerCase('A'); // minuscula = 'a'

        System.out.println("Es letra: " + isLetter);
        System.out.println("Es dígito: " + isDigit);
        System.out.println("Es espacio: " + isWhiteSpace);
        System.out.println("Mayúscula: " + upperText);
        System.out.println("Minúscula: " + lowerText);
    }
}
```

```java
package Booleans;

public class WrapperBoolean {
    public static void main(String[] args) {

        boolean value = Boolean.parseBoolean("true"); // valor = true
        System.out.println("El valor de 'value' es: " + value);

        Boolean wrapper = Boolean.valueOf("true"); // wrapper = true (como Boolean)
        System.out.println("El valor de 'wrapper' es: " + wrapper);

        String text = Boolean.toString(true); // texto = "true"
        System.out.println("El valor de 'text' es: " + text);

        boolean result = Boolean.logicalAnd(true, false); // resultado = false
        System.out.println("El resultado de 'Boolean.logicalAnd(true, false)' es: " + result);

        boolean result2 = Boolean.logicalOr(true, false); // resultado = true
        System.out.println("El resultado de 'Boolean.logicalOr(true, false)' es: " + result2);

    }
}
```

## Enlaces Relacionados
- [[Java.md]]
- [[Java/Clases y Objetos/01_Clases_y_objetos]]
- [[Java/Clases y Objetos/02_Atributos_y_metodos_de_clases]]
- [[Java/Clases y Objetos/03_Constructores]]
- [[Java/Clases y Objetos/04_Modificadores_de_acceso]]

#java #clases #wrapper
