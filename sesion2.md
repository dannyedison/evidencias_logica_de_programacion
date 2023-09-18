<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 2


<!-- Su documentación aquí -->
## 1. Programa para calcular la hipotenusa de un triángulo rectángulo:
Se ingresan dos valores de catetos (a y b)y se realiza la fórmula a²+b²= c² y se imprime el valor de la Hipotenusa (c).
``` java
package com.mycompany.hipotenusatriangulo;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class HipotenusaTriangulo {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el valor del primer cateto: ");
        double cateto1 = entraDato.nextDouble();

        System.out.print("Ingrese el valor del segundo cateto: ");
        double cateto2 = entraDato.nextDouble();

        //La fórmula del teorema de Pitágoras es: a²+b²= c²
        //Math.pow(base, exponente)
        //Math.sqrt() calcula raiz cuadrada
        double hipotenusa = Math.sqrt(Math.pow(cateto1, 2) + Math.pow(cateto2, 2)); 
        System.out.println("La hipotenusa del triángulo es: " + hipotenusa);

        entraDato.close();
    }
}
```

## 2. Programa para determinar si un número es par o impar:
Se ingresa un número, se calcula su Módulo 2, y si es resultado es 0, el número es par.
``` java
package com.mycompany.parimpar;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class ParImpar {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese un número: ");
        int numero = entraDato.nextInt();

        //Modulo, resto de una división
        //Si el Modulo es igual a 0, es un número par
        if (numero % 2 == 0) {
            System.out.println("El número es par.");
        } else {
            System.out.println("El número es impar.");
        }

        entraDato.close();
            
    }
}
``` 

## 3. Programa para calcular el tercer ángulo de un triángulo:
Se ingresan dos valores. Cada valor debe ser mayor a 0 y menor a 180. el rsulrado es 180 - (valor1 + valor2)
``` java
package com.mycompany.tercerangulotriangulo;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class TercerAnguloTriangulo {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el valor del primer ángulo: ");
        int angulo1 = entraDato.nextInt();

        System.out.print("Ingrese el valor del segundo ángulo: ");
        int angulo2 = entraDato.nextInt();

        //El valor ingresado no puede ser menor a 0 ni mayor a 180
        //El resultado es 180 menos la suma de los dos valores ingresados
        if (angulo1 > 0 && angulo1 < 180 && angulo2 > 0 && angulo2 < 180) {
            int tercerAngulo = 180 - (angulo1 + angulo2);
            System.out.println("El valor del tercer ángulo es: " + tercerAngulo);
        } else {
            System.out.println("Los valores ingresados no son ángulos válidos.");
        }

        entraDato.close();
        
    }
}
``` 

## 4. Programa para calcular el promedio de tres números:
Se ingresan tres valores, los cuales se suman y se dividen por 3: (valor1+valor2+valor3)/3
``` java
package com.mycompany.promediotresnumeros;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class PromedioTresNumeros {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        double numero1 = entraDato.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        double numero2 = entraDato.nextDouble();

        System.out.print("Ingrese el tercer número: ");
        double numero3 = entraDato.nextDouble();

        //La formula de promedio (n1+n2+n3)/3
        double promedio = (numero1 + numero2 + numero3) / 3;
        System.out.println("El promedio de los tres números es: " + promedio);

        entraDato.close();
    }
}
``` 

## 5. Programa para calcular la longitud de una cadena de texto:
Se ingresa una cadena de caracteres a una variable String, y con la función .legth(), se obtiene el tamaño de la cadena.
```java
package com.mycompany.longitudcadena;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class LongitudCadena {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese una cadena de texto: ");
        String texto = entraDato.nextLine();

        // texto.length() calcula longitud de String
        int longitud = texto.length();
        System.out.println("La longitud de la cadena es: " + longitud);

        entraDato.close();
    }
}
```

## 6. Programa para calcular el área de un triángulo:
se ingresan dos valores que corresponden a los 2 catetos, y se aplica la fórmula (base*altura)/2 para calcular la Hipotenusa.
```java
package com.mycompany.areatriangulo;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class AreaTriangulo {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        System.out.print("Ingrese la base del triángulo: ");
        double base = entraDato.nextDouble();

        System.out.print("Ingrese la altura del triángulo: ");
        double altura = entraDato.nextDouble();

        //Se ingresan 2 valores: base y altura
        //La formula del area del triangulo (base*altura)/2
        double area = (base * altura) / 2;
        System.out.println("El área del triángulo es: " + area);

        entraDato.close();
                
    }
}
```

## 7. Programa para calcular la raíz cuadrada de un número:
Se ingresa un valor, y con la función .Math.sqrt, se eleva éste valor al cuadrado.
```java
package com.mycompany.raizcuadrada;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class RaizCuadrada {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        System.out.print("Ingrese un número: ");
        double numero = entraDato.nextDouble();
        
        //Math.sqrt() calcula raiz cuadrada 
        double raizCuadrada = Math.sqrt(numero);
        System.out.println("La raíz cuadrada del número es: " + raizCuadrada);

        entraDato.close();
    }
}
```

## 8. Programa para calcular el máximo común divisor (MCD) de dos números:
Se ingresan dos valores a y b. El programa principar envía estos dos valores a una función donde por medio de un while y una operación de Módulo, se calcula el MCD. La función devuelve el último valor de b antes de ser 0.
``` java
package com.mycompany.maximocomundivisor;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class MaximoComunDivisor {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        System.out.print("Ingrese el primer número: ");
        int numero1 = entraDato.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero2 = entraDato.nextInt();

        //Envía a la función calcularMCD() los dos valores ingresados 
        int mcd = calcularMCD(numero1, numero2);
        System.out.println("El máximo común divisor de los dos números es: " + mcd);

        entraDato.close();
    }
    
    //Funcion entera que recibe 2 valores
    // el balor de b debe ser diferente de 0
    public static int calcularMCD(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
        //Cuando el modulo de a%b sea 0, termina el While y envía el valor anterior que tenía b antes de ser 0 
    }
}
```

## 9. Programa para imprimir una cadena de texto en orden inverso:
Se ingresa una cadena de texto, se calcula su tamaño con la función .length(), luego se crea un String nuevo y vacío, el cual se llenará con los valores de las posiciones que tiene el indice i-1 en el String ingresado.
```java
package com.mycompany.cadenainversa;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class CadenaInversa {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        System.out.print("Ingrese una cadena de texto: ");
        String texto = entraDato.nextLine();
        
        // texto.charAt() devuelve en un nuevo String el carácter de una cadena en la posición i. 
        //texto.length() indica el tamaño del String
        //A i se le asigna el valor del tamaño del String - 1
        String textoInverso = "";
        for (int i = texto.length() - 1; i >= 0; i--) {
            textoInverso += texto.charAt(i);
        }

        System.out.println("La cadena en orden inverso es: " + textoInverso);

        entraDato.close();
    }
}
```
## 10. Programa para calcular el área de un rectángulo:
Se ingresan dos valores corespondientes a la base y a la altura, y para calcular el área se aplica la formula base * altura.
``` java
package com.mycompany.arearectangulo;

/**
 *
 * @author 3D AUTOMATIZACION
 */
import java.util.Scanner;
public class AreaRectangulo {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        System.out.print("Ingrese la base del rectángulo: ");
        double base = entraDato.nextDouble();

        System.out.print("Ingrese la altura del rectángulo: ");
        double altura = entraDato.nextDouble();

        //Formula area = base * altura
        double area = base * altura;
        System.out.println("El área del rectángulo es: " + area);

        entraDato.close();
    }
}

```



