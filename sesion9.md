<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

## GRUPO
### Javier Boyacá
### Alejandro Aguirre
### Danny Edison Idarraga


## 2. Calculadora de la mediana


Codigo que calcula la Media de una serie de valores.

Despues de inicializar y llenar la lista, se calcula el tamaño de la lista y también se hace el ordenamiento de ésta.

En un IF(), se pregunta por el módulo 2 del tamaño de la lista. si el resultado es 0, el tamaño es Par, de lo contrario, el tamaño es Impar.

Si el tamaño es Par, el valor del tamaño se divide entre 2. el valor obtenido es la posición de la lista, que actua como indice (tempo), se toma el valor almacenado en esta posición y se le suma el valor almacenado en tempo-1, y luego el resultado se divide entre 2 para obtener el promedio.

Si el tamaño es Impar, el valor del tamaño se divide entre 2. el valor obtenido es la posición de la lista, que actua como indice, el valor almacenado en esta posición es la media de la lista.

```java
package com.mycompany.media;
import java.util.*;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Media {

    public static void main(String[] args) {
        
        int[] lista = {8,3,20,15,10,1,6,12,2,11}; //Llenado
        int totalDatos = lista.length; //Tamaño de la lista
        
        Arrays.sort(lista); // Ordenamiento de la lista
        
        for(int dato : lista){
            System.out.print(" ," + dato); // Imprimir la lista
        }
        
        if ((totalDatos % 2) == 0){//Si es 0, es par, diferente de 0 es impar
            //Par
            System.out.println(" Par");
            int tempo = totalDatos / 2;
            //System.out.println("tempo: " + tempo);
            //System.out.println("lista indice tempo: " + lista[tempo]);
            
            double media = (lista[tempo] + lista[tempo - 1])/2; //calculo promedio
            //int media = lista[totalDatos/2];
            System.out.println("Media: " + media); //Imprimir media
            
        } else {
            // Impar
            System.out.println(" impar");
            int media = lista[totalDatos/2];
            System.out.println("Media: " + media); //Imprimir media
        }
        
    }
}


```







