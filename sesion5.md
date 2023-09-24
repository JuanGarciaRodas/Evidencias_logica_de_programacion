<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->

# **Actividad 5: Ejercicios de bucles**

### Resolver los siguientes ejercicios:

## **Ejercicios - while**
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

## **Ejercicios - do while**
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

## **Ejercicios - for**

1. Imprimir los números impares del 1 al 50.

2. Imprimir los números primos del 1 al 100.

# Solucion

**Ejercicios - while**

- Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

 ```java

     import java.util.Scanner;
     class Main {
     public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);

         System.out.println("por favor digita cualquier numero: ");
        int numero = entradaDatos.nextInt();
        System.out.println("la tabla de multiplicar del " +numero+ " es: ");
        
        int i =1;
        while(i<=10){
            
            System.out.println( numero + "x" +i+ "=" +numero*i);
            
            i++;
            
        }
     }
     }
 ```
- Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

 ```java

     import java.util.Scanner;
     class Main {
     public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
      System.out.println("digita un texto  que contenga numeros: ");
        String cadena = entradaDatos.nextLine();
        
        int i =0;
        int contadorNumeros =0;
        while (i < cadena.length()) {
            
            char numero =cadena.charAt(i);
           
           if(Character.isDigit(numero)){
               contadorNumeros++;
           }
           i++;
           
           
            }
        System.out.println("la cantidad de numeros en el texto Son: "+contadorNumeros);
     }
     }
 ```

**Ejercicios - do while**

- Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

 ```java
     import java.util.Scanner;
     class Main {
      public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
     int i = 1;     
        System.out.println("Por favor digita un numero:");
        int numero =entradaDatos.nextInt();
           do {
            System.out.println(i);
         i++;         
        }while(i<=100 && numero >=0 ); 
     }
     }

 ```

- Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

 ```java

     import java.util.Scanner;
     class Main {
     public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
     System.out.println("por favor digita un  numero entero: ");
        int numero = entradaDatos.nextInt();
        System.out.println("la tabla de multiplicar del " +numero+ " es: ");
        
        int i =1;
        do{
            
            System.out.println( numero + "x" +i+ "=" +numero*i);
            
            i++;  
        }while(i<=10 && numero!=0);
     }
     }

 ```

**Ejercicios - for**

- Imprimir los números impares del 1 al 50.

 ```java

     class Main {
     public static void main(String[] args) {
     for (int i=1; i<=50; i+=2) {
            System.out.println(i);
            
            
        }
     }
     }

 ```

- Imprimir los números primos del 1 al 100.

 ```java

     class Main {
     public static void main(String[] args) {
     int max = 100;

        for (int i = 1; i <= max; i++) {
            int divisor = 0;
            for (int x = 1; x <= i / 2; x++) {
                if (i % x == 0) {
                    divisor += 2;

                }
                if (divisor > 2) {
                    break;
                }

            }
            if (divisor == 2) {
                System.out.println(i);

            }
        }
     }
     }

 ```



