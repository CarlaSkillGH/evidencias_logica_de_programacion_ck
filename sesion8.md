<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 

# Ejecicios de métodos en Java

Implementar los siguientes métodos:

## Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

```java
public static int encontrarMayor(int numero1, int numero2) {
    if (numero1 > numero2) {
        return numero1;
    } else {
        return numero2;
    }
}

```

## Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

```java
public static int contarVocales(String texto) {
    int contador = 0;
    String textoEnMinusculas = texto.toLowerCase();
    for (int i = 0; i < textoEnMinusculas.length(); i++) {
        char caracter = textoEnMinusculas.charAt(i);
        if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
            contador++;
        }
    }
    return contador;
}

```

## Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

```java
public static String cambiarMayusculasMinisculas(String texto) {
    StringBuilder resultado = new StringBuilder();
    for (int i = 0; i < texto.length(); i++) {
        char caracter = texto.charAt(i);
        if (Character.isUpperCase(caracter)) {
            resultado.append(Character.toLowerCase(caracter));
        } else if (Character.isLowerCase(caracter)) {
            resultado.append(Character.toUpperCase(caracter));
        } else {
            resultado.append(caracter);
        }
    }
    return resultado.toString();
}

```


## Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

```java
public static int contarPalabras(String texto) {
    String[] palabras = texto.split("\\s+");
    return palabras.length;
}

```


## Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

```java
import java.util.Arrays;

public static String ordenarPalabrasAlfabeticamente(String texto) {
    String[] palabras = texto.split("\\s+");
    Arrays.sort(palabras);
    return String.join(" ", palabras);
}

```