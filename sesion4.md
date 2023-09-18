<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->
## Actividad 4: Ejercicios de control de flujo con expresiones compuestas
``` java
package com.mycompany.actividad4;

/**
 *
 * @author 3D AUTOMATIZACION
 */
public class Actividad4 {

    public static void main(String[] args) {
        // Variables de tipo String
        String nombre = "Juan ";
        String apellido = "Pérez González";
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
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 1" );
        //Determinar si el estudiante es mayor de edad y tiene un estado activo.
        if (edad >= 18 && esActivo) {
            System.out.println("El estudiante es mayor de edad y está activo");
        }
        else {
            System.out.println("El esudiante es menor de edad o no está activo");
        }        
             
        System.out.println("--------------------------------------------------" );
        
        System.out.println("ACTIVIDAD 2" );
        //Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
        if (becado == true || carrera.equals("Desarrollo de Software") ) {
            System.out.println("El estudiante es becado o está en desarrollo de software");
        }
        else {
            System.out.println("El esudiante no es becado y no estudia desarrollo de software");
        }        
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 3" );
        //Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
        if (semestre == 3 && esActivo) {
            System.out.println("El estudiante está en último semestre y está activo");
        }
        else {
            System.out.println("El esudiante no está en último semestre o no está activo");
        }  
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 4" );
        //Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
        if (carrera.equals("Desarrollo de Software") && promedio>4.0) {
            System.out.println("El estudiante está en desarrollo de software y tiene promedio superior a 4.0");
        }
        else {
            System.out.println("El estudiante no está en desarrollo de software o no tiene promedio superior a 4.0");
        }  
                
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 5" );
        //Mostrar toda la información del estudiante si está matriculado en el Cesde.
        if (universidad.equals("Cesde")) {
            System.out.println("Nombre: " + nombre);
            System.out.println("Apellido: " + apellido);
            System.out.println("Identificación: " + identificación);
            System.out.println("Edad: " + edad);
            System.out.println("Género: " + género);
            System.out.println("Correo: " + correo);
            System.out.println("Carrera: " + carrera);
            System.out.println("Universidad: " + universidad);
            System.out.println("Activo: " + esActivo);
            System.out.println("Becado: " + becado);
            System.out.println("Promedio: " + promedio);
            System.out.println("Semestre: " + semestre);
        }
        else {
            System.out.println("El estudiante no está matriculado en Cesde");
        }  
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 6" );
        //Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
        if (universidad.equals("Cesde") && promedio>4.0 && esActivo) {
            System.out.println("Asignar beca del 50%");
        }
        else {
            System.out.println("No se puede asignar beca del 50%");
        }
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 7" );
        //Determinar la cantidad de beca que recibe el estudiante según su promedio:
        //0.0 - 3.4: El estudiante no recibe beca.
        //3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
        //4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
        //4.5 - 5.0: El estudiante recibe una beca completa.
        if (promedio >=0.0 && promedio <=3.4){
            System.out.println("El estudiante no recibe beca.");
        }
        else if (promedio >=3.5 && promedio <=3.9){
            System.out.println("El estudiante recibe beca del 25%.");
        }
        else if (promedio >=4.0 && promedio <=4.4){
            System.out.println("El estudiante recibe beca del 50%.");
        }
        else if (promedio >=4.5 && promedio <=5.0){
            System.out.println("El estudiante recibe beca completa.");
        }
        else {
            System.out.println("Nota no válida");
        }
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 8" );
        System.out.println("¿El alumno es mayor de edad?");
        
        System.out.println((edad>=18) ? "El alumno es mayor de edad: " + edad : "El alumno es menor de edad: " + edad);
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 9" );
        System.out.println("¿El alumno esta becado y es activo?");
        
        if (becado && esActivo) {
            System.out.println("El estudiante está becado y está activo");
        }
        else {
            System.out.println("El estudiante no está becado o no está activo");
        }  
        
        System.out.println("--------------------------------------------------" );

        System.out.println("ACTIVIDAD 10" );
        System.out.println("¿Cual es el género del alumno?");
        
        if (género == 'M'){
            System.out.println("El género del estudiante es masculino");
        }
        else if (género == 'F'){
            System.out.println("El género del estudiante femenino");
        }
        else{
            System.out.println("Género no definido");
        }
    }
}
```





