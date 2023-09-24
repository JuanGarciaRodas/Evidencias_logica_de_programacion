<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->
# Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

**Con la información anterior, implementa los siguientes ejercicios:**

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.

2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.

3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.

4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.

5. Mostrar toda la información del estudiante si está matriculado en el Cesde.

6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.

7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.

# Solucion

 ```java
     class Main {
     public static void main(String[] args) {
     // Variables de tipo String
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
     // Variable de tipo int
        int edad = 20;
     // Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
     // Variable de tipo char
        char genero = 'M';
     // Variable de tipo double
        double promedio = 4.5;
     // Variable de tipo int
        int semestre = 2;
        //  Determinar si el estudiante es mayor de edad y tiene un estado activo.
        System.out.println(".....................................");
        System.out.println("Ejercicio 1");
        if (edad > 18 && esActivo);
        {
            System.out.println("El estudiante es mayor de edad y esta activo");
        }

        //Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
        System.out.println(".....................................");
        System.out.println("Ejercicio 2");
        if (becado || carrera.equals("Desarrollo de Software")) {
            System.out.println("Cumple una o las dos condiciones");
        }
     //Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
        System.out.println(".....................................");
        System.out.println("Ejercicio 3");
        if (semestre == 3 && esActivo) {
            System.out.println("El estudiante cumple con las condiciones");
        } else {
            System.out.println("no cumple las condiciones");
        }
        //Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
        System.out.println(".....................................");
        System.out.println("Ejercicio 4");
        if (carrera.equals("Desarrollo de Software") && promedio >= 4.0) {
            System.out.println("el estudiante cumple con las condiciones");
        }
     //Mostrar toda la información del estudiante si está matriculado en el Cesde.
        System.out.println(".....................................");
        System.out.println("Ejercicio 5");
        if (universidad.equals("Cesde")) {
            System.out.println("Nombre del estudiante: " + nombre + "\nApellido del  estudiante: " + apellido
                    + "\nNumero de identrificacion: " + identificación + "\nCorreo: " + correo + "\nNombre de carrera: " + carrera
                    + "\nUniversidad: " + universidad + "\nEdad: " + edad + "\nEstado del estudiante: " + esActivo + "\nTiene alguna beca: " + becado
                    + "\nGenero: " + genero + "\nPromedio del estudiante: " + promedio + "\nSemestre: " + semestre);
        } else {
            System.out.println("El estudiante no esta matriculado en el cesde");
        }
     //Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
        System.out.println(".....................................");
        System.out.println("Ejercicio 6");

        if (universidad.equals("Cesde") && promedio >= 4.0 && esActivo) {
            System.out.println("El etudiante obtuvo una beca del 50%");
        } else {
            System.out.println("El estudiante perdio la beca");
        }
        //Determinar la cantidad de beca que recibe el estudiante según su promedio:
     //0.0 - 3.4: El estudiante no recibe beca.
     //3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
     //4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
     //4.5 - 5.0: El estudiante recibe una beca completa. 
        System.out.println(".....................................");
        System.out.println("Ejercicio 7");
        System.out.println("Determinar la cantidad de beca que recibe el estudiante según su promedio:\n"
                + "0.0 - 3.4: El estudiante no recibe beca.\n"
                + "3.5 - 3.9: El estudiante recibe una beca parcial del 25%.\n"
                + "4.0 - 4.4: El estudiante recibe una beca parcial del 50%.\n"
                + "4.5 - 5.0: El estudiante recibe una beca completa.");
        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no puede obtener una beca ");

        } else if (promedio >= 3.4 && promedio <= 3.9) {
            System.out.println("El estudiante obtiene una beca parcial del 25%. ");

        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante obtiene una beca parcial del 50%");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante se ha ganado una beca completa");

        }
        // 
        //Determinar si el estudiante pasa al siguiente semestre de acuerdo a su promedio
        System.out.println(".....................................");
        System.out.println("Ejercicio 8");
        if (promedio >= 4.5);
       

            System.out.println("EL estudiente continua al siguiente semestre");
            
            // si el estudiante es menor de edad debe ir acompañado de un adulto a la excursion
      System.out.println(".....................................");
        System.out.println("Ejercicio 9");
        
        if (edad >=18)
            System.out.println("Puede Ir solo a la excursion");
        
        else {
            System.out.println("de ir acompañado de un adulto");
        } 
        // identificar si el estudiante es Hombre o tiene identificacion para ser representante
      System.out.println(".....................................");
        System.out.println("Ejercicio 10"); 
        
        if (genero == 'M' || identificación.equals ("1000000001"));
        System.out.println("Es elegido como representante");
     }
     }
 ```





