<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->
## Actividad 5: Ejercicios de bucles

## Ejercicios - while

### 1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

### 2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

``` java
package com.mycompany.actwhile;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class ActWhile {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.println("Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.");
        System.out.println("Ingresar un número para conocer su tabla de multiplicar");
        int numero = entraDato.nextInt();
        int i = 0;

        while (i <= 10) {
            System.out.println("Resultado " + i + " * " + numero + " = " + (i * numero));
            i++;
        }

        System.out.println("-------------------------------------------");


        System.out.println("Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.");

        Scanner entraCadena = new Scanner(System.in);
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = entraCadena.nextLine();

        int contadorNumeros = 0;
        i = 0;
        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (caracter == '0' || caracter == '1' || caracter == '2' || caracter == '3' || caracter == '4'
                    || caracter == '5' || caracter == '6' || caracter == '7' || caracter == '8' || caracter == '9') {
                contadorNumeros++;
            }
            i++;
        }
        System.out.println("La cadena ingresada contiene " + contadorNumeros + " números.");

    }
}
```

## Ejercicios - do while

### 1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

### 2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

``` java
package com.mycompany.actdowhile;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class ActDoWhile {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        System.out.println("Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.");
        System.out.println("Ingrese un numero negativo para detener: ");
        int numero = entraDato.nextInt();
        int i = 1;

        if (numero > 0) {
            do {
                System.out.println("Resultado: " + i); // realiza esta operacion al menos una vez asi no se cumpla la condicion
                i++;
            } while (i <= 100);
        }

        System.out.println("-----------------------------------------------------------------------");


        System.out.println("Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.");
        System.out.println("Ingrese un numero entero o 0 para detener");
        numero = entraDato.nextInt();
        i = 0;

        if (numero != 0) {
            do {
                System.out.println("Resultado " + i + " * " + numero + " = " + (i * numero)); // realiza esta operacion al menos una vez asi no se cumpla la condicion
                i++;
            } while (i <= 10);

        }

    }
}
```

## Ejercicios - for

### 1. Imprimir los números impares del 1 al 50.

### 2. Imprimir los números primos del 1 al 100.

``` java
package com.mycompany.actfor;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class ActFor {

    public static void main(String[] args) {
        System.out.println("Imprimir los números impares del 1 al 50.");

        for (int i = 1; i < 50; i += 2) {
            System.out.println(i);
        }

        System.out.println("-------------------------------------------");


        System.out.println("Imprimi Ir los números primos del 1 al 100.");

        //int j;
       // boolean esPrimo;
        for (int x = 2; x <= 100; x++) {
            int j = 2;
            boolean esPrimo = true;
            while (j <= x / 2) {
                if (x % j == 0) {
                    esPrimo = false;
                    break;
                }
                j++;
            }
            if (esPrimo) {
                System.out.println(x + " es número primo.");
            } 

        }
    }
}

```




