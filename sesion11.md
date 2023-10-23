<!-- No borrar o modificar -->
[Inicio](./index.md)

# Sesión 11 

## Programa en Java para detectar números repetidos

### Sintaxis 1 de Java

```java
import java.util.HashSet;

public class Ejercicio1 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2, 3, 4};

        // Creamos una estructura de datos para almacenar los números repetidos
        HashSet<Integer> numerosRepetidos = new HashSet<>();
        HashSet<Integer> numerosVistos = new HashSet<>();

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            if (!numerosVistos.add(numeros[i])) {
                // El número actual ya ha aparecido
                numerosRepetidos.add(numeros[i]);
            }
        }

        // Si existen números repetidos, los imprimimos
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son:");
            for (int numero : numerosRepetidos) {
                System.out.println(numero);
            }
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

## Programa en Java para convertir números binarios a decimales

### Sintaxis 2 de Java

```java
public class BinaryToDecimal {
    public static void main(String[] args) {
        long binario = 101010; // Número binario a convertir
        int decimal = convertirBinarioADecimal(binario);
        System.out.println("El número binario " + binario + " en decimal es: " + decimal);
    }

    // Función para convertir binario a decimal
    public static int convertirBinarioADecimal(long binario) {
        int decimal = 0;
        int potencia = 0;
        while (binario != 0) {
            long digito = binario % 10;
            decimal += digito * Math.pow(2, potencia);
            binario /= 10;
            potencia++;
        }
        return decimal;
    }
}
```





