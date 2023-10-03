<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 

# Ejercicios de bucles

Resolver los siguientes ejercicios:

## Ejercicios - while

1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

```java
import java.util.Scanner;
/**
 *
 * @author CESDE
 */
public class ActividadCinco {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Ingresa un número para mostrar su tabla de multiplicar hasta 10: ");
        int numero = sc.nextInt();

        System.out.println("Tabla de multiplicar del " + numero + ":");
        for (int i = 1; i <= 10; i++) {
            int resultado = numero * i;
            System.out.println(numero + " x " + i + " = " + resultado);
        }

        sc.close();
    }
}
```

2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

```java
import java.util.Scanner;

public class ActividadCinco {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Ingresa una cadena de caracteres: ");
        String cadena = sc.nextLine();

        int contadorNumeros = 0;

        for (int i = 0; i < cadena.length(); i++) {
            char caracter = cadena.charAt(i);
            if (Character.isDigit(caracter)) {
                contadorNumeros++;
            }
        }

        System.out.println("La cantidad de caracteres que son números en la cadena es: " + contadorNumeros);

        sc.close();
    }
}
```

## Ejercicios - do while

1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

```java
import java.util.Scanner;

public class ActividadCinco {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int numero = 1;
        while (numero >= 1 && numero <= 100) {
            System.out.println(numero);
            System.out.print("Ingresa un número negativo para detener la secuencia: ");
            numero = sc.nextInt();
        }

        System.out.println("Fin del programa");

        sc.close();
    }
}
```

2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

```java
import java.util.Scanner;

public class ActividadCinco {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Ingresa un número entero para obtener su tabla de multiplicar (0 para salir): ");
        int numero = sc.nextInt();

        while (numero != 0) {
            System.out.println("Tabla de multiplicar del " + numero + ":");
            for (int i = 1; i <= 10; i++) {
                int resultado = numero * i;
                System.out.println(numero + " x " + i + " = " + resultado);
            }

            System.out.print("Ingresa otro número (0 para salir): ");
            numero = sc.nextInt();
        }

        System.out.println("Fin del programa");

        sc.close();
    }
}
```

##  Ejercicios - for

1. Imprimir los números impares del 1 al 50.

```java
public class ActividadCinco {
    public static void main(String[] args) {
        System.out.println("Números impares del 1 al 50:");
        for (int i = 1; i <= 50; i += 2) {
            System.out.println(i);
        }
    }
}

```

2. Imprimir los números primos del 1 al 100.

```java
public class ActividadCinco {
    public static void main(String[] args) {
        System.out.println("Números primos del 1 al 100:");

        for (int numero = 2; numero <= 100; numero++) {
            boolean esPrimo = true;

            for (int divisor = 2; divisor < numero; divisor++) {
                if (numero % divisor == 0) {
                    esPrimo = false;
                    break;
                }
            }

            if (esPrimo) {
                System.out.println(numero);
            }
        }
    }
}
```






