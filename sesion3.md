<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 

# Ejercicios de operaciones básicas en Java.

## 1. Suma y multiplicación

Ejemplo de un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

```java
import java.util.Scanner;
public class SumaMultiplicacion {
    public static void main(String[] args) {
        // Crear un objeto Scanner para leer la entrada del usuario
        Scanner sc = new Scanner(System.in);
        
        // Solicitar al usuario que ingrese el primer número entero
        System.out.print("Ingrese el primer número entero: ");
        int numero1 = sc.nextInt();
        
        // Solicitar al usuario que ingrese el segundo número entero
        System.out.print("Ingrese el segundo número entero: ");
        int numero2 = sc.nextInt();
        
        // Calcular la suma de los números
        int suma = numero1 + numero2;
        
        // Calcular la multiplicación de los números
        int multiplicacion = numero1 * numero2;
        
        // Imprimir la suma y la multiplicación
        System.out.println("La suma de " + numero1 + " y " + numero2 + " es: " + suma);
        System.out.println("La multiplicación de " + numero1 + " y " + numero2 + " es: " + multiplicacion);
        
        // Cerrar el objeto Scanner
        sc.close();
    }
}
```

## 2. Resta y división

```java
import java.util.Scanner;

public class RestaDivision {
    public static void main(String[] args) {
        // Crear un objeto Scanner para leer la entrada del usuario
        Scanner sc = new Scanner(System.in);

        // Solicitar al usuario que ingrese el primer número entero
        System.out.print("Ingrese el primer número entero: ");
        int numero1 = sc.nextInt();

        // Solicitar al usuario que ingrese el segundo número entero
        System.out.print("Ingrese el segundo número entero: ");
        int numero2 = sc.nextInt();

        // Calcular la resta de los números
        int resta = numero1 - numero2;

        // Asegurarse de que el segundo número no sea cero para evitar la división por cero
        if (numero2 != 0) {
            // Calcular la división de los números
            double division = (double) numero1 / numero2;

            // Imprimir la resta y la división
            System.out.println("La resta de " + numero1 + " y " + numero2 + " es: " + resta);
            System.out.println("La división de " + numero1 + " entre " + numero2 + " es: " + division);
        } else {
            System.out.println("No se puede realizar la división debido a que el segundo número es cero.");
        }

        // Cerrar el objeto Scanner
        sc.close();
    }
}

```

## 3. Operaciones combinadas

```java
import java.util.Scanner;

public class OperacionesCombinadas {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa el primer número entero: ");
        int num1 = sc.nextInt();
        
        System.out.print("Ingresa el segundo número entero: ");
        int num2 = sc.nextInt();
        
        System.out.print("Ingresa el tercer número entero: ");
        int num3 = sc.nextInt();
        
        int suma = num1 + num2 + num3;
        int multiplicacion = num1 * num2;
        double division = (double) multiplicacion / num3;
        
        System.out.println("La suma de los tres números es: " + suma);
        System.out.println("La multiplicación del primer número por el segundo es: " + multiplicacion);
        System.out.println("La división del resultado entre el tercer número es: " + division);
        
        sc.close();
    }
}
```

## 4. Operaciones combinadas

```java
import java.util.Scanner;

public class OperacionesDecimales {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa el primer número decimal: ");
        double num1 = sc.nextDouble();
        
        System.out.print("Ingresa el segundo número decimal: ");
        double num2 = sc.nextDouble();
        
        double suma = num1 + num2;
        double resta = num1 - num2;
        double multiplicacion = num1 * num2;
        double division = num1 / num2;
        
        System.out.println("La suma es: " + suma);
        System.out.println("La resta es: " + resta);
        System.out.println("La multiplicación es: " + multiplicacion);
        System.out.println("La división es: " + division);
        
        sc.close();
    }
}
``` 
## 5. Operaciones con decimales

```java
import java.util.Scanner;
/**
 *
 * @author CESDE
 */
public class ActividadTres {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa el primer número decimal: ");
        double num1 = sc.nextDouble();
        
        System.out.print("Ingresa el segundo número decimal: ");
        double num2 = sc.nextDouble();
        
        double suma = num1 + num2;
        double resta = num1 - num2;
        double multiplicacion = num1 * num2;
        double division = num1 / num2;
        
        System.out.println("La suma es: " + suma);
        System.out.println("La resta es: " + resta);
        System.out.println("La multiplicación es: " + multiplicacion);
        System.out.println("La división es: " + division);
        
        sc.close();
    }
}

``` 

## 6. Incremento y decremento

```java
public class ActividadTres {
    public static void main(String[] args) {
        int numero = 10;
        
        System.out.println("Valor inicial: " + numero);
        
        numero++;
        System.out.println("Valor después de incrementar en 1: " + numero);
        
        numero--;
        System.out.println("Valor después de decrementar en 1: " + numero);
    }
}

``` 

## 7. Operador de asignación compuesta

```java
public class ActividadTres {
    public static void main(String[] args) {
        int numero = 7;
        
        System.out.println("Valor inicial: " + numero);
        
        numero += 5;
        System.out.println("Valor después de sumar 5: " + numero);
    }
}

``` 

## 8. Operadores lógicos

```java
import java.util.Scanner;

public class ActividadTres {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa el primer valor booleano (true o false): ");
        boolean valor1 = sc.nextBoolean();
        
        System.out.print("Ingresa el segundo valor booleano (true o false): ");
        boolean valor2 = sc.nextBoolean();
        
        boolean and = valor1 && valor2;
        boolean or = valor1 || valor2;
        boolean not1 = !valor1;
        boolean not2 = !valor2;
        
        System.out.println("Resultado de AND: " + and);
        System.out.println("Resultado de OR: " + or);
        System.out.println("Resultado de NOT para el primer valor: " + not1);
        System.out.println("Resultado de NOT para el segundo valor: " + not2);
        
        sc.close();
    }
}

``` 

## 9. Operador ternario

```java
import java.util.Scanner;

public class ActividadTres {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa un número entero: ");
        int numero = sc.nextInt();
        
        String resultado = (numero >= 0) ? "positivo" : "negativo";
        
        System.out.println("El número ingresado es " + resultado + ".");
        
        sc.close();
    }
}

``` 











