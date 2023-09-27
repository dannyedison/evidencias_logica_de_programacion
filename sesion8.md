<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

### 1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

```java
package com.mycompany.actividad1;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
//Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
public class Actividad1 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int numero1 = entraDato.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero2 = entraDato.nextInt();

        //Envía a la función mayor 
        int numeroMayor = mayor(numero1, numero2);
        System.out.println("El números mayor es: " + numeroMayor);

        entraDato.close();
    }

    /*Funcion entera que recibe 2 valores
    y retorna un valor*/
    public static int mayor(int a, int b) {
        if (a > b) {
            return a;
        } else if (b > a) {
            return b;
        } else {
                return a;
             //Cuando a y b son iguales
        }
    }
}

```

### 2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

```java
package com.mycompany.actividad2;
import java.util.Scanner;
/**
 *
 * @author 3D AUTOMATIZACION
 */
//Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
public class Actividad2 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = sc.nextLine();
        
        //Envía la cadena de caracteres
        int resultado = cuentaVocales(cadena);
        System.out.println("El número de vocales es: " + resultado);

        sc.close();
    }
    
    //Funcion entera que recibe un String y devuleve el número de vocales
    public static int cuentaVocales(String cadena) {
        int i = 0;
        int contadorVocales = 0;

        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u' ||
                caracter == 'A' || caracter == 'E' || caracter == 'I' || caracter == 'O' || caracter == 'U') {
                contadorVocales++;
            }
            i++;
        }
        return contadorVocales;
    }
}

```

### 3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

```java

```

### 4.Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

```java
public class Actividad4 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = sc.nextLine();
        
        //Llamado del método
        int contador = cuentaPalabras(cadena);
        System.out.println("La cadena tiene " + contador + " palabras");

    }
    
    //Funcion entera que recibe un String y devuleve el número de palabras
    public static int cuentaPalabras(String cadena) {
        int contadorPalabras = cadena.split("\\s").length;
        return contadorPalabras;
    }
}

```

### 5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

```java

```