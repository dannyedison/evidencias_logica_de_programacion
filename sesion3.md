<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->
## Actividad 3: Ejercicios de operaciones básicas en Java.
### 1. Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

``` java
package com.mycompany.act1;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act1 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int num1 = entraDato.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int num2 = entraDato.nextInt();

        int suma = num1 + num2;
        int mult = num1 * num2;
        
        System.out.println("número 1 + número 2: " + suma);
        System.out.println("número 1 * número 2: " + mult);

        entraDato.close();
    }
}
```

### 2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números. 
``` java
package com.mycompany.act2;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act2 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int num1 = entraDato.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int num2 = entraDato.nextInt();

        int resta = num1 - num2;
        int div = num1 / num2;
        
        System.out.println("número 1 - número 2: " + resta);
        System.out.println("número 1 / número 2: " + div);

        entraDato.close();
    }
}
```

### 3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.
``` java
package com.mycompany.act3;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act3 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int num1 = entraDato.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int num2 = entraDato.nextInt();
        
        System.out.print("Ingrese el tercer número: ");
        int num3 = entraDato.nextInt();

        int suma = num1 + num2 + num3;
        int multi = num1 * num2;
        int division = multi / num3;
        
        System.out.println("número 1 + número 2 + número 3: " + suma);
        System.out.println("número 1 * número 2: " + multi);
        System.out.println("(número 1 * número 2) / número 3: " + division);

        entraDato.close();
    }
}
```

### 4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.
``` java
package com.mycompany.act4;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act4 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese el primer número decimal: ");
        double num1 = entraDato.nextDouble();

        System.out.print("Ingrese el segundo número decimal: ");
        double num2 = entraDato.nextDouble();

        double suma = num1 + num2;
        double resta = num1 - num2;
        double mult = num1 * num2;
        double div = num1 / num2;
        
        System.out.println("número 1 + número 2: " + suma);
        System.out.println("número 1 - número 2: " + resta);
        System.out.println("número 1 * número 2: " + mult);
        System.out.println("número 1 / número 2: " + div);

        entraDato.close();
    }
}
```

### 5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.
``` java
package com.mycompany.act5;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act5 {

    public static void main(String[] args) {
        int num1 = 25;
        num1++; //incrementar 1        
        System.out.println("número: " + num1);
        num1--; //decrementar 1
        System.out.println("número: " + num1);
        
        //otra forma
        int num2 = 25;
        num2 += 1; //incrementar 1        
        System.out.println("número: " + num2);
        num2 -= 1; //decrementar 1
        System.out.println("número: " + num2);
        
    }
}
```

### 6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.
``` java
package com.mycompany.act6;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act6 {

    public static void main(String[] args) {
        int num1 = 25;
        num1 +=5;        
        System.out.println("número 1 + 5: " + num1);
               
                       
    }
}
```

### 7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.
``` java
package com.mycompany.act7;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act7 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);
        
        boolean resultado;
        System.out.println("Ingrese en número 1: true o false");
        boolean num1 = entraDato.nextBoolean();
        
        System.out.println("Ingrese en número 2: true o false");
        boolean num2 = entraDato.nextBoolean();
        
        resultado =  num1 && num2;
        System.out.println("número 1 AND número 2: " + resultado);
        
        resultado =  num1 || num2;
        System.out.println("número 1 OR número 2: " + resultado);
        
        resultado =  !num1;
        System.out.println("resultado NOT número 1: " + resultado);
        
        resultado =  !num2;
        System.out.println("resultado NOT número 2: " + resultado);
        
        entraDato.close();      
        
    }
}
```

### 8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.
``` java
package com.mycompany.act8;

import java.util.Scanner;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Act8 {

    public static void main(String[] args) {
        Scanner entraDato = new Scanner(System.in);

        System.out.print("Ingrese un número: ");
        int num1 = entraDato.nextInt();
        
        System.out.print((num1>0) ? "El número es positivo: " + num1 : "El número es negativo: " + num1);
        
        entraDato.close();
    }
}
```





