<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->




# **Ejercicios de Lógica de Programación**

1. **Crear un programa en Java para calcular el interés de un CDT**

Un CDT (Certificado de Depósito a Término) es un producto financiero en el que un inversor deposita una cantidad de dinero en un banco por un plazo determinado y a cambio recibe una tasa de interés fija. Al final del plazo, el inversor recupera su inversión inicial más los intereses generados. Aquí hay un ejemplo de cómo crear un programa en Java para calcular el interés de un CDT:

2. **Calcular la cantidad de materiales necesarios para construir una pared de ladrillos**

Cálculo de la cantidad de materiales para la construcción: Este ejercicio consiste en calcular la cantidad de materiales necesarios para construir una estructura. Para ello, se debe tener en cuenta las dimensiones de la estructura y la cantidad de materiales necesarios por unidad de área o de volumen. Algunos ejemplos de cálculos de materiales son el cálculo de la cantidad de ladrillos necesarios para construir una pared, o el cálculo de la cantidad de concreto necesario para una losa o columna.


# SOLUCION

- **Crear un programa en Java para calcular el interés de un CDT**


     ```java
         package com.mycompany.ejercicioslogicaactividad10;
         import java.util.Scanner;
         import java.text.DecimalFormat;
          /**
         *
         * @author Juan Carlos
          */
          public class EjerciciosLogicaActividad10 {

         public static void main(String[] args) {
      
         DecimalFormat decimalFormat = new DecimalFormat("#,###");
         Scanner scanner = new Scanner(System.in);

           System.out.println("Bienvenido al calculador de CDT!");

          // Pedir al usuario que ingrese los datos del CDT
         System.out.print("Ingrese el monto del depósito: ");
         double montoDeposito = scanner.nextDouble();

         System.out.print("Ingrese la tasa de interés anual (%): ");
         double tasaInteresAnual = scanner.nextDouble();

         System.out.print("Ingrese el plazo en meses: ");
         int plazoMeses = scanner.nextInt();

         // Calcular el interés y el monto total al vencimiento
         double tasaInteresMensual = tasaInteresAnual / 12 / 100;
         double interesMensual = montoDeposito * tasaInteresMensual;
         double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

         // Mostrar el resumen del CDT
         System.out.println("Resumen del CDT:");
          System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
         System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
         System.out.println("- Plazo en meses: " + plazoMeses);
         System.out.println("- Interés mensual: $" + interesMensual);
         System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
         }
         }
     ```



- **Calcular la cantidad de materiales necesarios para construir una pared de ladrillos**

     ```java
         package com.mycompany.actividad10;
         import java.util.Scanner;
         /**
          *
          * @author Juan Carlos
          */
         public class Actividad10 {

          public static void main(String[] args) {
          Scanner input = new Scanner(System.in);
          double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;
      
          // Solicita las dimensiones de la pared
          System.out.print("Ingrese el largo de la pared en metros: ");
          largo = input.nextDouble();
         System.out.print("Ingrese el alto de la pared en metros: ");
          alto = input.nextDouble();
         System.out.print("Ingrese el ancho de la pared en metros: ");
          ancho = input.nextDouble();

          // Solicita las dimensiones del ladrillo
         System.out.print("Ingrese el largo del ladrillo en metros: ");
          largoLadrillo = input.nextDouble();
         System.out.print("Ingrese el alto del ladrillo en metros: ");
         altoLadrillo = input.nextDouble();
         System.out.print("Ingrese el ancho del ladrillo en metros: ");
         anchoLadrillo = input.nextDouble();

          // Calcula el área de la pared y del ladrillo
         areaPared = largo * alto;
          double areaLadrillo = largoLadrillo * altoLadrillo;

          // Calcula la cantidad de ladrillos necesarios
         cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));

         // Muestra el resultado en la consola
         System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
         } 
         }
     ```