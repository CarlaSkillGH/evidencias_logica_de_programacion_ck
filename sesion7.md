<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 

## Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

### Ejemplo Array

```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

### Ejemplo Array list

```java
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }
```

```java
  public static void agregarNota (ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

## Array en Java:
Un array en Java es una estructura de datos que almacena elementos del mismo tipo en una ubicación contigua en memoria con un tamaño fijo.

```java
public class ActividadSiete {
    public static void main(String[] args) {
        // Declarar e inicializar un array de enteros
        int[] numeros = new int[5];

        // Asignar valores a los elementos del array
        numeros[0] = 1;
        numeros[1] = 2;
        numeros[2] = 3;
        numeros[3] = 4;
        numeros[4] = 5;

        // Acceder y mostrar elementos del array
        for (int i = 0; i < numeros.length; i++) {
            System.out.println("Elemento " + i + ": " + numeros[i]);
        }
    }
}
```

## ArrayList en Java:
Un ArrayList en Java es una colección dinámica que puede crecer o disminuir de tamaño automáticamente. A diferencia de un array, un ArrayList puede contener elementos de diferentes tipos.

```java
import java.util.ArrayList;

public class ActividadSiete {
    public static void main(String[] args) {
        // Declarar e inicializar un ArrayList de enteros
        ArrayList<Integer> numeros = new ArrayList<Integer>();

        // Agregar elementos al ArrayList
        numeros.add(1);
        numeros.add(2);
        numeros.add(3);
        numeros.add(4);
        numeros.add(5);

        // Acceder y mostrar elementos del ArrayList
        for (int i = 0; i < numeros.size(); i++) {
            System.out.println("Elemento " + i + ": " + numeros.get(i));
        }
    }
}
```

## Principales diferencias entre un array y un ArrayList en Java:

1. ### Tamaño

Un array tiene un tamaño fijo que se especifica al momento de la creación, mientras que un ArrayList puede cambiar de tamaño dinámicamente según sea necesario.


2. ### Tipo de elementos

En un array, todos los elementos deben ser del mismo tipo, mientras que en un ArrayList, puedes almacenar elementos de diferentes tipos si se declaró con un tipo genérico.


3. ### Métodos: 

 Los ArrayList proporcionan una variedad de métodos útiles para agregar, eliminar y manipular elementos, lo que facilita la gestión de colecciones de datos en comparación con los arrays, que requieren una gestión manual más tediosa.

En resumen, los ArrayList son más flexibles y fáciles de usar en comparación con los arrays estáticos en Java.