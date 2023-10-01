<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->


# **Actividad: Ejecicios Array - ArrayList**


## En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

#### **Ejemplo Array**

 ```java

      import java.util.Arrays;

     public class EjercicioArray {

     public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
     }
     }
 ```

#### **Ejemplo Array list**

 ```java
      import java.util.ArrayList; 
     import java.util.Scanner;

     public class AppNotas {

      public static void main(String[] args) {

     ArrayList<String> notas = new ArrayList<>();
    
     Scanner scan = new Scanner(System.in);

     while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

     }

     }

     public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
     System.out.println("Ingrese el titulo de la nota:");
     String titulo = scan.nextLine();
    
     System.out.println("Ingrese el contenido de la nota:");
     String contenido = scan.nextLine();
    
     notas.add(titulo + " - " + contenido);

     }

       public static void mostrarNotas(ArrayList<String> notas) {

     for(String n : notas) {
      System.out.println(n);
     }

     }

     }

 ```
 
 
## Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

#### **Solucion**


## Arrays

 ```java
         package com.mycompany.arrayas;
          java.util.Arrays;
         /**
         *
          * @author Juan Carlos
         */
          public class Arrayas {
         // Imprimir el arrays
     
         public static void main(String[] args) {
         String [] Empresas = new String [7];
        
         Empresas [0] = "Coordinadora";
         Empresas [1] = "Exito";
         Empresas [2] = "Sura";
         Empresas [3] = "Americanino";
         Empresas [4] = "Diesel";
         Empresas [5] = "Yamaha";
         Empresas [6] = "Toyota";
        
         for(int i=0; i<Empresas.length; i++) {
                System.out.println(Empresas [i]);
         }
         }
                
         }
 ```



## Arraylist


 ```java

     package com.mycompany.arraylist;

     import java.util.ArrayList;

     /**
      *
     * @author Juan Carlos
     */
     public class Arraylist {

     public static void main(String[] args) {
        ArrayList<String> Familia = new ArrayList<>();

        Familia.add("Juan Carlos");
        Familia.add("Juan Pablo");
        Familia.add("Luciana");
        Familia.add("Natalia");
        Familia.add("Luna");

        for (String Famili : Familia) {
            System.out.println(Familia);

        }
       
     }
     }
 ```