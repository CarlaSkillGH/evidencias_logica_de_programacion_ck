<!-- No borrar o modificar -->
[Inicio](./index.md)

# Sesión 9 

## jercicios de Lógica de Programación

### Sintaxis calculadora de resistencias eléctricas

Una resistencia eléctrica es un componente electrónico que se utiliza para limitar el flujo de corriente eléctrica en un circuito. Es decir, su función es oponerse al paso de la corriente eléctrica y disminuir su intensidad.

Las resistencias se componen generalmente de un material conductor, como el carbono o el metal, que se coloca en un cuerpo cerámico o de vidrio. El valor de la resistencia (es decir, la cantidad de oposición que ofrece al paso de la corriente eléctrica) se mide en ohms, y depende de la composición del material y de su geometría.

Las resistencias se utilizan en una gran variedad de circuitos electrónicos, tanto en circuitos analógicos como digitales. Algunas de las aplicaciones más comunes de las resistencias incluyen la limitación de corriente en circuitos de alimentación, el ajuste de niveles de voltaje y corriente en circuitos de amplificación, y la medición de corriente y voltaje en circuitos de control y monitoreo.

Calculadora Código de colores - Online

https://www.digikey.com/es/resources/conversion-calculators/conversion-calculator-resistor-color-code


```java
public class SesionNueve {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String bandaDeColor1;
        String bandaDeColor2;
        String bandaDeColor3;

        System.out.println("Calculadora de resistencias eléctricas en ohmios");
        System.out.println("Las resistencias eléctricas se calculan mediante un código de colores en el que los valores están asociados a colores.");
        System.out.println("Color Negro = 0");
        System.out.println("Color Marrón = 1");
        System.out.println("Color Rojo = 2");
        System.out.println("Color Naranja = 3");
        System.out.println("Color Amarillo = 4");
        System.out.println("Color Verde = 5");
        System.out.println("Color Azul = 6");
        System.out.println("Color Púrpura = 7");
        System.out.println("Color Gris = 8");
        System.out.println("Color Blanco = 9");

        System.out.println("Ingrese el primer color");
        int negro = 0;
        int marron = 1;
        int rojo = 2;
        int naranja = 3;
        int amarillo = 4;
        int verde = 5;
        int azul = 6;
        int purpura = 7;
        int gris = 8;
        int blanco = 9;

        bandaDeColor1 = scanner.nextLine().toLowerCase(); // Convierte la entrada a minúsculas

        switch (bandaDeColor1) {
            case "negro":
                break;
            case "marron":
                break;
            case "rojo":
                break;
            case "naranja":
                break;
            case "amarillo":
                break;
            case "verde":
                break;
            case "azul":
                break;
            case "purpura":
                break;
            case "gris":
                break;
            case "blanco":
                break;
            default:
                System.out.println("Valor invalido 1");
                return;
        }

        System.out.println("Ingrese el segundo color");
        bandaDeColor2 = scanner.nextLine().toLowerCase(); // Convierte la entrada a minúsculas

        switch (bandaDeColor2) {
            case "negro":
                break;
            case "marron":
                break;
            case "rojo":
                break;
            case "naranja":
                break;
            case "amarillo":
                break;
            case "verde":
                break;
            case "azul":
                break;
            case "purpura":
                break;
            case "gris":
                break;
            case "blanco":
                break;
            default:
                System.out.println("Valor invalido 2");
                return;
        }

        System.out.println("Ingrese el tercer color");
        bandaDeColor3 = scanner.nextLine().toLowerCase(); // Convierte la entrada a minúsculas

        int resultadoBanda1 = 0;
        int resultadoBanda2 = 0;
        int resultadoBanda3 = 0;

        switch (bandaDeColor1) {
            case "negro":
                resultadoBanda1 = negro;
                break;
            case "marron":
                resultadoBanda1 = marron;
                break;
            case "rojo":
                resultadoBanda1 = rojo;
                break;
            case "naranja":
                resultadoBanda1 = naranja;
                break;
            case "amarillo":
                resultadoBanda1 = amarillo;
                break;
            case "verde":
                resultadoBanda1 = verde;
                break;
            case "azul":
                resultadoBanda1 = azul;
                break;
            case "purpura":
                resultadoBanda1 = purpura;
                break;
            case "gris":
                resultadoBanda1 = gris;
                break;
            case "blanco":
                resultadoBanda1 = blanco;
                break;
            default:
                System.out.println("Valor invalido 3");
                return;
        }

        switch (bandaDeColor2) {
            case "negro":
                resultadoBanda2 = negro;
                break;
            case "marron":
                resultadoBanda2 = marron;
                break;
                case "rojo":
                resultadoBanda2 = rojo;
                break;
            case "naranja":
                resultadoBanda2 = naranja;
                break;
            case "amarillo":
                resultadoBanda2 = amarillo;
                break;
            case "verde":
                resultadoBanda2 = verde;
                break;
            case "azul":
                resultadoBanda2 = azul;
                break;
            case "purpura":
                resultadoBanda2 = purpura;
                break;
            case "gris":
                resultadoBanda2 = gris;
                break;
            case "blanco":
                resultadoBanda2 = blanco;
                break;
            default:
                System.out.println("Valor invalido 4");
                return;
        }

        switch (bandaDeColor3) {
            case "negro":
                resultadoBanda3 = negro;
                break;
            case "marron":
                resultadoBanda3 = marron;
                break;
            case "rojo":
                resultadoBanda3 = rojo;
                break;
            case "naranja":
                resultadoBanda3 = naranja;
                break;
            case "amarillo":
                resultadoBanda3 = amarillo;
                break;
            case "verde":
                resultadoBanda3 = verde;
                break;
            case "azul":
                resultadoBanda3 = azul;
                break;
            case "purpura":
                resultadoBanda3 = purpura;
                break;
            case "gris":
                resultadoBanda3 = gris;
                break;
            case "blanco":
                resultadoBanda3 = blanco;
                break;
            default:
                System.out.println("Valor invalido 5");
                return;
        }

        int resultadoFinal = (resultadoBanda1 * 10 + resultadoBanda2) * (int) Math.pow(10, resultadoBanda3);
        System.out.println("El valor de la resistencia es: " + resultadoFinal + " ohmios");
```





