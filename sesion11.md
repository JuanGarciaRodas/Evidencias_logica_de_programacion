<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

# **Actividad: Ejercicios de Lógica de Programación**

- Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

- Desarrollar un algoritmo que realice la conversión de binario a decimal.

# **Solucion**

- Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.


 ```java 

     package com.mycompany.actividad11;

     import java.util.HashSet;

     /**
     *
      * @author Juan Carlos
     */
      public class Actividad11 {

     public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 3, 5, 2, 5, 1};

        // Creamos un conjunto para almacenar los números que aparecen más de una vez
        HashSet<Integer> numerosRepetidos = new HashSet<>();
        HashSet<Integer> numerosUnicos = new HashSet<>();

        // Recorremos el conjunto de números
        for (int numero : numeros) {
            // Si el número ya está en el conjunto de números únicos, lo agregamos al conjunto de repetidos
            if (numerosUnicos.contains(numero)) {
                numerosRepetidos.add(numero);
            } else {
                // Si no está en el conjunto de números únicos, lo agregamos a ese conjunto
                numerosUnicos.add(numero);
            }
        }

        // Si hay números repetidos, los imprimimos
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
     }
     }


 ```




- Desarrollar un algoritmo que realice la conversión de binario a decimal.

  ```java
       package com.mycompany.binarioadecimal;
  
     /**
     *
     * @author Juan Carlos
      */
      public class Binarioadecimal {

     public static void main(String[] args) {
        String numeroBinario = "1010101010"; // Cambia esto al número binario que desees convertir
        int numeroDecimal = binarioADecimal(numeroBinario);
        System.out.println("El número binario " + numeroBinario + " es igual a " + numeroDecimal + " en decimal.");
     }

     public static int binarioADecimal(String numeroBinario) {
        int longitud = numeroBinario.length();
        int numeroDecimal = 0;

        for (int i = 0; i < longitud; i++) {
            char bit = numeroBinario.charAt(i);
            int valorBit = Character.getNumericValue(bit);

            // Añadimos el valor del bit a la suma acumulada
            numeroDecimal += valorBit * Math.pow(2, longitud - 1 - i);
        }

        return numeroDecimal;
     }
     }


  ```