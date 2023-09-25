<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->
## Actividad: Ejecicios Array - ArrayList

### 1. Probar, analizar y explicar el funcionamiento del siguiente ejemplo de Array.

``` java
package com.mycompany.arrayejemplo;

import java.util.Arrays;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class ArrayEjemplo {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1}; //Crear asignar Array

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            //Recorre cada posicion del Array y va sumando cada número y almacena el resultado
            suma += numeros[i]; 
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0]; //Asigna en "maximo" el valor que está en la posición 0 del Array números
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) { 
                //Si el número en la posición i del Array "numero" es mayor que el valor que tiene "maximo",
                //entonces el valor de "maximo" es reemplazado por el número en la posición i del Array "numero"
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        //El método .sort() ordena los elementos de un array 
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

### 2. Probar, analizar y explicar el funcionamiento del siguiente ejemplo de Array list

``` java
package com.mycompany.arraylistejemplo;

import java.util.ArrayList; 
import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class ArrayListEjemplo {

    public static void main(String[] args) {
        ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);
    
    // El while en true asegura el ingreso al ciclo
    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  //Ir a la función agregarNotas si digita 1
      } else if (opcion == 2) {
        mostrarNotas(notas); //Ir a la función mostrarNotas si digita 2
      } else {
        break; //Si digita 3 o no digita un valor válido, interrumpe el while
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    // La funcion recibe 2 valores: el arraylist y la variable scan
      
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    //Adiciona el contenido de título de la materia y la nota al ArrayList notas
    //materia y nota estan concatenados
    notas.add(titulo + " - " + contenido);
    
    // La funcion devuelve 2 valores: el arraylist y la variable scan

  }

  public static void mostrarNotas(ArrayList<String> notas) {
      // La función recibe un valor del ArrayList

    for(String n : notas) {
      System.out.println(n);
      //Imprime n con los valores del ArrayList 
    }

  }

}
```

### 3. Crear un ejemplo de Array.

Este código calcúla la cantidad de numeros pares e impares en un Array

```java
package com.mycompany.arrayactividad;
import java.util.Arrays;

/**
 *
 * @author 3D AUTOMATIZACION
 * 
 * Programa para calcular la cantidad de numeros pares e impares en un Array
 */
public class ArrayActividad {

    public static void main(String[] args) {
        int[] numeros = {8, 5, 15, 4, 1, 10, 6, 13, 2}; //Crear y asignar Array

        // Imprimir Array
        System.out.println("Array Original: " + Arrays.toString(numeros));

        // Calcular cantidad de numeros PARES
        int sumaPar = 0;
        int sumaImpar = 0;
        for (int i = 0; i < numeros.length; i++) {
            //Recorre cada posicion del Array y suma la cantidad de numeros pares
            if (numeros[i]%2 == 0){
                sumaPar ++;
            }
            else {
                // Suma la cantidad de números impares
                sumaImpar ++;
            }
        }
        System.out.println("La cantidad de números del Array es: " + numeros.length);
        System.out.println("La cantidad de números pares es: " + sumaPar);
        System.out.println("La cantidad de números impares es: " + sumaImpar);
    }
}

```

### 4. Crear un ejemplo de ArrayList.

En este código se usaron métodos para el ingreso de los númeos, imprimir el ArrayList y el ordenamiento e impresión del ArrayList.

```java
package com.mycompany.arraylistactividad;

import java.util.ArrayList;
import java.util.Scanner;
import java.util.Collections; 

/**
 *
 * @author 3D AUTOMATIZACION
 */
//Pograma que permite ingresar numero a un ArrayList
//Imprime el ArrayList tal como se ingresó y Ordenado
public class ArrayListActividad {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Integer> numeros = new ArrayList<>();

        // El while en true asegura el ingreso al ciclo
        while (true) {
            System.out.println("");
            System.out.println("1 Agregar Números");
            System.out.println("2 Mostrar Números Ingresados");
            System.out.println("3 Mostrar Números Ordenados");
            System.out.println("4 Salir");
            System.out.println("");

            int opcion = sc.nextInt();
            //Evalúa la condición con el número ingresado
            if (opcion == 1) {
                agregarNumeros(numeros, sc);  //Ir a la función agregarNumeros si digita 1
            } else if (opcion == 2) {
                mostrarNumeros(numeros); //Ir a la función mostrarNumeros si digita 2
            } else if (opcion == 3) {
                mostrarNumerosOrdenados(numeros); //Ir a la función mostrarNumeros si digita 2
            } else {
                break; //Si digita 4 o no digita un valor válido, interrumpe el while
            }
        }
    }

    public static void agregarNumeros(ArrayList<Integer> numeros, Scanner sc) {
        // La funcion recibe 2 valores: el ArrayList y la variable sc

        System.out.println("Ingrese un Número");
        int numeroIngresado = sc.nextInt();
        //Adiciona el número ingresado
        numeros.add(numeroIngresado);
    }

    public static void mostrarNumeros(ArrayList<Integer> numeros) {
        // La función recibe un valor del ArrayList
        System.out.println("Números Ingresados");
        for (int n : numeros) {
            System.out.print(n + " ,");
            //Imprime n con los valores del ArrayList 
        }
        System.out.println("");
    }

    public static void mostrarNumerosOrdenados(ArrayList<Integer> numeros) {
        // La función recibe un valor del ArrayList

        Collections.sort(numeros);  // Ordenar ArrayList
        System.out.println("Números Ordenados");
        for (int n : numeros) {
            System.out.print(n + " ,");
            //Imprime n con los valores del ArrayList Ordenados
        }
        System.out.println("");
    }
}

```



