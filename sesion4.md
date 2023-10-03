<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

# Ejercicios de control de flujo con expresiones compuestas

```java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
    - 0.0 - 3.4: El estudiante no recibe beca.
    - 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
    - 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
    - 4.5 - 5.0: El estudiante recibe una beca completa.

```java
import java.util.Scanner;

/**
 *
 * @author CESDE
 */
public class ActividadCuatro {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        // Variables de tipo String
        String nombre = "Joan Sebastian";
        String apellido = "González";
        String identificación = "111";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        boolean carreraDeSo = true;
        String universidad = "Cesde";
        // Variable de tipo int
        int edad = 20;
        // Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
        // Variable de tipo char
        char género = 'M';
        // Variable de tipo double
        double promedio = 4.5;
        // Variable de tipo int
        int semestre = 2;

        System.out.println(" >---Ejercicio 1---< ");
        if (edad >= 18 && esActivo) {
            System.out.println("El estudiante es mayor de edad y está activo");
        }

        System.out.println(" >---Ejercicio 2---< ");
        if (carreraDeSo || becado) {
            System.out.println("Aplica");
        }
        if (carrera == "Desarrollo de Software") {
            System.out.println("Es estudiante de Desarrollo de Software");
        } else {
            System.out.println("No es estudiante de Desarrollo de Software");
        }

        if (becado) {
            System.out.println("El estudiante es becado");
        } else {
            System.out.println("El estudiante no es becado");
        }
        System.out.println(" >---Ejercicio 3---< ");
        if (esActivo && semestre >= 3) {
            System.out.println("Activo en su último semestre");
        } else if (esActivo || semestre >= 3) {
            System.out.println("Cumple con alguna de las dos condiciones");
        }
        if (semestre >= 3) {
            System.out.println("El estudiante está en su último semestre");
        } else {
            System.out.println("El estudiante aun no está en su último semestre");

        }
        System.out.println(" >---Ejercicio 4---< ");
        if (carreraDeSo) {
            System.out.println("El estudiante está haciendo una carrera relacionada al Desarrollo de Software");
        } else {
            System.out.println("El estudiante no está haciendo una carrera relacionada al Desarrollo de Software");
        }
        if (promedio >= 4.0) {
            System.out.println("Su promedio es excelente");
        } else {
            System.out.println("Su promedio puede mejorar");
        }
        System.out.println(" >---Ejercicio 5---< ");
       
        System.out.println("Ingrese el nombre o documento del estudiante: ");
    String datos = sc.nextLine();

    switch (datos) {
      case "Joan Sebastian":
        System.out.println (identificación + " " + correo);
        break;
      case "111":
          System.out.println(carrera + " " + universidad);
        break;  
      default:
        System.out.println("Día no válido");
    }
        System.out.println(" >---Ejercicio 6---< ");
        if(esActivo && promedio >= 4.0)
            System.out.println("El estudiante es apto para una beca del 50% de descuento");
        else{
            System.out.println("El estudiante no es apto para una beca del 50% de descuento");

        System.out.println(" >---Ejercicio 7---< ");
        
            System.out.print("Ingresa el promedio del estudiante: ");
        double promedio = sc.nextDouble();
        
        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%.");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");
        } else {
            System.out.println("El promedio ingresado no es válido.");
        }
        
        sc.close();
    }
}
