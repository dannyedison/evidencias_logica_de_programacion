<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

## Prueba, ejecución y explicación de ejercicios de lógica de programación.

1. Crear un programa en Java para calcular el interés de un CDT
Un CDT (Certificado de Depósito a Término) es un producto financiero en el que un inversor deposita una cantidad de dinero en un banco por un plazo determinado y a cambio recibe una tasa de interés fija. Al final del plazo, el inversor recupera su inversión inicial más los intereses generados. 



```java
package com.mycompany.calculocdt;

import java.util.Scanner;
import java.text.DecimalFormat;// clase que da formato a números decimales

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class CalculoCDT {

    public static void main(String[] args) {
        DecimalFormat decimalFormat = new DecimalFormat("#,###"); //Usado para imprimir los resuldados
        Scanner scanner = new Scanner(System.in); //crea a scanner para el ingreso de datos

        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble(); //ingresa el monto del deposito

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();//ingresa la tasa de interes anual

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();//ingresa plazo en meses

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;//calcula la tasa de interes mensual
        double interesMensual = montoDeposito * tasaInteresMensual;//cacula el interes que se genera mensualmente
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);//calcula cuanto recibirá al finalizar el tiempo de la inversión

        // Mostrar el resumen del CDT
        //Imprime las variables con sus textos asociados
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + interesMensual);
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}

```

7. Cálculo del costo de energía eléctrica de un electrodoméstico
Para calcular el costo de energía eléctrica de un electrodoméstico, se deben seguir los siguientes pasos: Determinar la potencia del electrodoméstico en vatios. Esta información se puede encontrar en la etiqueta del electrodoméstico o en el manual del usuario.

Determinar el tiempo de uso diario del electrodoméstico en horas. Este valor puede variar dependiendo del usuario y del electrodoméstico. Determinar el precio por unidad de energía eléctrica. Este valor se encuentra en la factura de energía eléctrica o se puede consultar con el proveedor de energía eléctrica.

Calcular el consumo diario del electrodoméstico en kilovatios-hora (kWh) multiplicando la potencia del electrodoméstico por el tiempo de uso diario y dividiendo el resultado entre 1000. La fórmula es: consumo_diario = (potencia * tiempo_de_uso_diario) / 1000.

Calcular el consumo mensual del electrodoméstico en kilovatios-hora multiplicando el consumo diario por el número de días del mes. La fórmula es: consumo_mensual = consumo_diario * días_del_mes.

Calcular el costo mensual de energía eléctrica del electrodoméstico multiplicando el consumo mensual por el precio por unidad de energía eléctrica. La fórmula es: costo_mensual = consumo_mensual * precio_por_unidad.

Por ejemplo, si un electrodoméstico tiene una potencia de 1200 vatios y se utiliza durante 4 horas al día, y el precio por unidad de energía eléctrica es de $0.12 por kWh, el cálculo del costo mensual de energía eléctrica sería:

consumo_diario = (1200 * 4) / 1000 = 4.8 kWh
consumo_mensual = 4.8 * 30 = 144 kWh
costo_mensual = 144 * 0.12 = 17.28 dólares

Por lo tanto, el costo mensual de energía eléctrica del electrodoméstico sería de 17.28 dólares.

```java
package com.mycompany.calculoconsumo;
import java.util.Scanner;
/**
 *
 * @author 3D AUTOMATIZACION
 */
public class CalculoConsumo {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

      // Solicitar datos al usuario
      System.out.print("Ingrese la potencia del electrodoméstico (en vatios): ");
      double potencia = input.nextDouble(); //ingreso de potencia
      
      System.out.print("Ingrese el tiempo de uso diario (en horas): ");
      double tiempoUsoDiario = input.nextDouble();//ingreso uso diario en horas
      
      System.out.print("Ingrese el precio por kilovatio-hora (en pesos): ");
      double precioKwh = input.nextDouble();//ingreso precio del kvh
      
      System.out.print("Ingrese el número de días del mes: ");
      int diasDelMes = input.nextInt();//ingreso dias de uso al mes
      
      // Cálculo del consumo mensual en kilovatios-hora
      double consumoDiarioKwh = (potencia * tiempoUsoDiario) / 1000; //calcula el consumo diario
      double consumoMensualKwh = consumoDiarioKwh * diasDelMes;// el consumo diario lo multiplica por los dias de uso al mes
      
      // Cálculo del costo mensual de energía eléctrica
      double costoEnergiaElectrica = consumoMensualKwh * precioKwh / 1000; // se divide entre 1000 para convertir el precio por kilovatio-hora en pesos
      
      // Imprimir el resultado en pantalla
      System.out.printf("El costo mensual de energía eléctrica es de: $%,.2f pesos", costoEnergiaElectrica);//imprime e costo mensual. el valor se muetra con 2 decimales. todas las variables son de tipo double

    }
}
  

```
