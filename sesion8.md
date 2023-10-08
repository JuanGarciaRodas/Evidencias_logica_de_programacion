<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->

# **Actividad: Ejecicios de métodos en Java**
## Implementar los siguientes métodos:

- Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# **SOLUCION**

- **Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.**

 ```java
     package com.mycompany.metodos1;

     import java.util.Scanner;

     /**
     *
        * @author Juan Carlos
     */
     //Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
        public class Metodos1 {

     static int maximo(int a, int b ){
     int max=0;
        if (a>b) 
            max=a;
         else 
            max=b;
        
        return(max);
     }
     public static void main (String[]args) {
     Scanner sc=new Scanner(System.in);
     int max=0;
     int a=0,b=0;
      System.out.println("Intrdoduzca un numero");
     a=sc.nextInt();
     System.out.println("Intrdoduzca otro numero");
     b=sc.nextInt();
    
     max =maximo (a, b);
     System.out.println("El numero mayor es:" +max);
    
     }
     }

 ```


- **Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.**

 ```java
         package com.mycompany.contador_vocales;

     /**
      *
      * @author Juan Carlos
     */
     //Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
         public class Contador_vocales {


     public static void main(String[] args) {
        String texto = "Ejemplo de texto con vocales";
        int numeroDeVocales = contarVocales(texto);
        System.out.println("El número de vocales en el texto es: " + numeroDeVocales);
     }

      public static int contarVocales(String texto) { 
        int contador = 0;
        texto = texto.toLowerCase(); // Convertimos el texto a minúsculas para hacer la comparación más sencilla.

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }

        return contador;
     }
     }


  ```


- **Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.**

 ```java
     package com.mycompany.mayusculasyminusculas;

     /**
     *
     * @author Juan Carlos
     */
     //Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
     public class Mayusculasyminusculas {

     public static void main(String[] args) {
        String texto = "jUAN cARLOS eStUDiante DeL CeSDE lOGiCa De proGRAMACION";
        String textoModificado = alternarMayusculasMinisculas(texto);
        System.out.println("Texto modificado: " + textoModificado);
     }

     public static String alternarMayusculasMinisculas(String texto) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter); // Mantener caracteres no alfabéticos sin cambios
            }
        }

        return resultado.toString();
     }
     }


 ```


 - **Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.**

 ```java
        package com.mycompany.numeropalabras;

     /**
     *
     * @author Juan Carlos
      */
     //Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
     public class Numeropalabras {


     public static void main(String[] args) {
        String texto = "La vida es mejor siempre sonriendo a cada instante";
        int numeroDePalabras = contarPalabras(texto);
        System.out.println("El número de palabras en el texto es: " + numeroDePalabras);
     }

     public static int contarPalabras(String texto) {
        if (texto == null || texto.isEmpty()) {
            return 0; // Si la cadena es nula o vacía, no hay palabras.
        }

        // Dividir la cadena en palabras utilizando el espacio en blanco como separador.
        String[] palabras = texto.split("\\s+");
        return palabras.length;
     }
     }

 ```


- **Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.**

 ```java
     package com.mycompany.palabrasenorden;
     import java.util.Arrays;
     /**
     *
     * @author Juan Carlos
     */
     //Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.
     public class Palabrasenorden {

     public static String ordenarPalabras(String texto) {
        // Dividir la cadena en palabras
        String[] palabras = texto.split("\\s+");

        // Ordenar las palabras alfabéticamente
        Arrays.sort(palabras);

        // Unir las palabras ordenadas en una nueva cadena
        String textoOrdenado = String.join(" ", palabras);

        return textoOrdenado;
     }

     public static void main(String[] args) {
        // Ejemplo de uso:
        String textoOriginal = "Mi mundo verde pagina web sobre la conciencia del reciclaje";
        String textoOrdenado = ordenarPalabras(textoOriginal);
        System.out.println(textoOrdenado);
     }
     }


 ```

 