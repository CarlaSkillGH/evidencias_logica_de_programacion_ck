<!-- No borrar o modificar -->
[Inicio](./index.md)

# Sesión 10 


## Programa en Java para calcular el interés de un CDT

### Sintaxis de Java

```JAVA
import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    public static void main(String[] args) {
        DecimalFormat decimalFormat = new DecimalFormat("#,###");
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble();

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;
        double interesMensual = montoDeposito * tasaInteresMensual;
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

        // Mostrar el resumen del CDT
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + interesMensual);
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}
```

A continuación, proporcionaré una explicación detallada de cómo funciona este programa:

El programa comienza por importar la clase Scanner y DecimalFormat.

Se crea una instancia de DecimalFormat con el patrón #,### para formatear los números con separadores de coma.

Se crea una instancia de Scanner para tomar la entrada del usuario.

Se muestra un mensaje de bienvenida al usuario.

Se solicita al usuario que ingrese el monto del depósito, la tasa de interés anual y el plazo en meses utilizando el objeto Scanner.

Se calcula la tasa de interés mensual dividiendo la tasa de interés anual por 12 y 100.

Se calcula el interés mensual multiplicando el monto del depósito por la tasa de interés mensual.

Se calcula el monto total al vencimiento sumando el monto del depósito con el producto del interés mensual y el plazo en meses.

Se muestra un resumen detallado de los detalles del CDT, incluyendo el monto del depósito, la tasa de interés anual, el plazo en meses, el interés mensual y el monto total al vencimiento, utilizando el formato de número decimal para mostrar cantidades grandes de manera legible.

El programa es útil para comprender cómo se pueden realizar cálculos financieros simples utilizando Java y cómo interactuar con la entrada del usuario a través de la consola.

## Cálculo del costo de energía eléctrica de un electrodoméstico

### Sintaxis de Java

```JAVA
import java.util.Scanner;

public class CalculoCostoEnergiaElectrica {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      // Solicitar datos al usuario
      System.out.print("Ingrese la potencia del electrodoméstico (en vatios): ");
      double potencia = input.nextDouble();
      
      System.out.print("Ingrese el tiempo de uso diario (en horas): ");
      double tiempoUsoDiario = input.nextDouble();
      
      System.out.print("Ingrese el precio por kilovatio-hora (en pesos): ");
      double precioKwh = input.nextDouble();
      
      System.out.print("Ingrese el número de días del mes: ");
      int diasDelMes = input.nextInt();
      
      // Cálculo del consumo mensual en kilovatios-hora
      double consumoDiarioKwh = (potencia * tiempoUsoDiario) / 1000;
      double consumoMensualKwh = consumoDiarioKwh * diasDelMes;
      
      // Cálculo del costo mensual de energía eléctrica
      double costoEnergiaElectrica = consumoMensualKwh * precioKwh / 1000; // se divide entre 1000 para convertir el precio por kilovatio-hora en pesos
      
      // Imprimir el resultado en pantalla
      System.out.printf("El costo mensual de energía eléctrica es de: $%,.2f pesos", costoEnergiaElectrica);
   }
}
```

Este ejercicio de Java realiza cálculos relacionados con el consumo de energía eléctrica en un hogar y calcula el costo mensual en dólares en función del consumo mensual y el costo por kilovatio hora (kWh).

El código proporcionado no está completo, pero parece ser una parte de un programa más amplio que realiza estos cálculos. Aquí tienes una explicación detallada de las operaciones realizadas en el código:

1. `consumo_diario = (1200 * 4) / 1000 = 4.8 kWh`: Esta línea calcula el consumo diario de electricidad en kilovatios hora (kWh) multiplicando 1200 vatios (que es igual a 1.2 kilovatios) por 4 horas y luego dividiendo el resultado entre 1000 para convertirlo en kilovatios hora.

2. `consumo_mensual = 4.8 * 30 = 144 kWh`: Esta línea calcula el consumo mensual de electricidad en kilovatios hora multiplicando el consumo diario por 30 días. Se asume un mes de 30 días para simplificar el cálculo.

3. `costo_mensual = 144 * 0.12 = 17.28 dólares`: Esta línea calcula el costo mensual en dólares multiplicando el consumo mensual en kilovatios hora por el costo por kilovatio hora, que es de 0.12 dólares en este caso.

En resumen, este código permite calcular el consumo diario y mensual de electricidad, así como el costo mensual en dólares, en función del consumo y del costo por kilovatio hora. Este tipo de cálculos son comunes en aplicaciones que proporcionan estimaciones de costos de consumo de energía eléctrica para ayudar a los usuarios a controlar y gestionar su consumo de energía.






