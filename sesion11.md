<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

## Actividad: Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

### Solución:
Por facilidad, el Array de números ingresado se ordena de menor a mayor, y luego se identifican los grupos de números repetidos y se van imprimiendo un número del grupo a medida que se van encontrando.

``` java

package com.mycompany.numrepetidos;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class NumRepetidos {

    public static void main(String[] args) {
        int min = 0;
        // Declaramos Array de números enteros
        int[] numeros = {6, 2, 1, 10, 4, 5, 10, 8, 2, 9, 5, 12, 11, 12};
        // Ordenamiento del array
        int aux;
        for (int i = 0; i < numeros.length; i++) {

            for (int j = 0; j < numeros.length; j++) {
                if (numeros[j] > numeros[i]) {
                    min = j;

                    aux = numeros[i];
                    numeros[i] = numeros[j];
                    numeros[j] = aux;
                }
            }
        }

        System.out.println("El vector ordenado es: ");
        //Imprimir el Array ordenado
        for (int i = 0; i < numeros.length; i++) {
            System.out.print(numeros[i] + ", ");
        }
        System.out.println(" ");
        System.out.print("Los números repetidos son: ");
        int pos = 0;
        //Rutina para identificar los numeros repetidos
        while (pos < numeros.length - 1) {
            //Identificar si el valor apuntado por el indice es igual al apuntado por el indice + 1
            if (numeros[pos] == numeros[pos + 1] && (pos < (numeros.length - 1))) {
                int j = 1;
                //si es verdad, identifica cuantos mas son iguales al valor apuntado por el indice
                while ((numeros[pos] == numeros[pos + j]) && ((pos + j) < (numeros.length - 2))) {
                    j++;
                }
                //cuando ya dejó de ser igual, imprime el valor
                System.out.print(numeros[pos] + ", ");
                //inicia el indice a la posición despues de los números repetidos
                pos += j+1;
                
            } else {
                //si no encuentra número repetido, incrementa el indice
                pos++;
            }
        }
    }
}

```

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

### Solución
En el número binario, inicialmente se identifica la primera cifra de derecha a izquierda usando el %. Luego, esta cifra se multiplica por la base 2 correspondiente.
Despues se elimina esta cifra para continual con la siguiente y aplicar el mismo proceso.



```java
package com.mycompany.bintodecimal;

import java.util.*;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Bintodecimal {

    public static void main(String[] args) {
        long numBinario;
        long ultimaCifra;
        long numDecimal=0;
        int exponente= 0;

        numBinario = 1010;
        exponente = 0;
        numDecimal = 0; //contendrá el número decimal
        while (numBinario != 0) {
            ultimaCifra = numBinario % 10; //encontrar la última cifra
            //multiplicar la cifra por 2 exponente correspondiente y se suma al decimal                          
            numDecimal = numDecimal + ultimaCifra * (int) Math.pow(2, exponente);
            exponente++; //incrementar el exponente
           
            numBinario = numBinario / 10;  //eliminar la última cifra
        }
        System.out.println("El Número Decimal es: " + numDecimal);
    }
}

```





