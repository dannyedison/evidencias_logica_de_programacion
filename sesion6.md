<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 6


<!-- Su documentación aquí -->

# PROYECTO INTEGRADOR

## GRUPO 4
### Javier Boyacá
### Alejandro Aguirre
### Danny Edison Idarraga

## TEMA:
## RESISTENCIAS ELÉCTRICAS 
### AGORITMO 1
## Aplicación para practicar los colores d la resistencias y su valor equivalente.


## PROGRAMA PRINCIPAL
```java
package com.mycompany.codigo1;

import java.util.*;
//import java.util.Arrays;

/**
 *
 * @author 3D AUTOMATIZACION
 *
 * LOGICA DE PROGRAMACIÓN
 *
 * Desarrollado por: GRUPO 4 Javier Boyacá Alejandro Aguirre Danny Edison
 * Idarraga
 *
 */
public class Codigo1 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("¡BIENVENIDO!");
        System.out.println("Programa para practicar el uso del código de colores en electrónica");
        System.out.println("¡Buena suerte!");

        int continuar = 0;

        while (continuar == 0) {
            System.out.println("Presiona '1' si quieres adivinar el color");
            System.out.println("Presiona '2' si quieres adivinar el valor del color");
            
            int seleccion = sc.nextInt();
            
            if (seleccion == 1) {
                advColor();
            } else if (seleccion == 2) {
                advNumero();
            } else {
                System.out.println("Valor no VÁLIDO");
            }
            System.out.println("Presione '0' para CONTINUAR u otro valor para TERMINAR");
            continuar = sc.nextInt();
        }
    }


```
En el programa principal, se da una corta bienvenida al usuario, al igual que se le explica la finalidad del juego.

El usurario tiene dos OPCIONES PARA JUGAR
1. Si quiere adivinar el color de acuerdo a un valor mostrado.
2. Si quiere adivinar el valor equivalente al color mostrado.


## MÉTODO advColor()


```java
    public static void advColor() {
        Scanner sc = new Scanner(System.in);

        //Asignación y llenado del Array
        String[] colorAlmacenado = {"NEGRO", "CAFE", "ROJO", "NARANJA", "AMARILLO", "VERDE", "AZUL", "MORADO", "GRIS", "BLANCO"};

        System.out.println("Recuerda que los colores son: MORADO, AMARILLO, CAFE, BLANCO, ROJO, GRIS, NARANJA, VERDE, NEGRO, AZUL");
        System.out.println("Digitar el color correspondiente al valor mostrado: ");
        System.out.println("");
        //Generación de un número aleatorio
        int numero = (int) (Math.random() * 10 + 0);

        System.out.println("Número: " + numero);
        System.out.print("Color: ");

        //Ingreso del color
        String cadena = sc.nextLine();
        String colorIngresado = cadena.toUpperCase();

        /*String sCadena = "Esto Es Una Cadena De TEXTO";
        System.out.println(sCadena.toLowerCase());*/
        System.out.println("");
        System.out.println("Color ingresado: " + colorIngresado);
        System.out.println("Color esperado: " + colorAlmacenado[numero]);
        System.out.println("");

        //Condicional
        if (colorAlmacenado[numero].equals(colorIngresado)) {
            System.out.println("¡FELICITACIONES! Has acertado");
            System.out.println("");
        } else {
            System.out.println("¡AAAH! El color digitado no es el correto. ¡Intenta de nuevo!");
            System.out.println("");
        }
    }
```
Cuando el usurario elije la opción 1., se ejecuta el método advColor(), en donde se le muestra al usuario los colores disponibles y se le presenta un valor aleatorio entre '0 y 9', y con dicho valor, debe escribir el color correspondiente al npumero mostrado.

Si el usuario acierta, se mostrará un mensaje de felicitación, de lo contrario, se mostrara un mensaje indicando que la respuesta no fue la correcta.

## MÉTODO advNumero()

```java
public static void advNumero() {
        Scanner sc = new Scanner(System.in);

        //Asignación y llenado del Array
        String[] colorAlmacenado = {"NEGRO", "CAFE", "ROJO", "NARANJA", "AMARILLO", "VERDE", "AZUL", "MORADO", "GRIS", "BLANCO"};

        System.out.println("Recuerda que los valores van de '0' al '9'");
        System.out.println("Digitar el valor correspondiente al color mostrado: ");
        System.out.println("");
        //Generación de un número aleatorio
        int numero = (int) (Math.random() * 10 + 0);

        System.out.println("Color: " + colorAlmacenado[numero]);
        System.out.print("Valor: ");

        //Ingreso del color
        int valorIngresado = sc.nextInt();

        System.out.println("");
        System.out.println("Valor ingresado: " + valorIngresado);
        System.out.println("Color " + colorAlmacenado[numero] + " equivalente al número: " + numero);
        System.out.println("");

        //Condicional
        if (numero == valorIngresado) {
            System.out.println("¡FELICITACIONES! Has acertado");
            System.out.println("");
        } else {
            System.out.println("¡AAAH! El valor digitado no es el correto. ¡Intenta de nuevo!");
            System.out.println("");
        }
    }

}

```

Cuando el usurario elije la opción 2., se ejecuta el método advNumero(), en donde se le muestra al usuario un color, y con éste, el usuario deberá digitar el valor entre '0 y 9'equivalente al color.

Si el usuario acierta, se mostrará un mensaje de felicitación, de lo contrario, se mostrara un mensaje indicando que la respuesta no fue la correcta.
 
