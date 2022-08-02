# 2 weeks
# Lunes

Lectura de If (else)

    La sentencia if, else es una funcion que nos permite validar si una accion es 
    verdadera o falsa, dependiendo de la validación se ejecuta y ya realizada su
    finalidad, se cierra el programa.

Lectura de sentencia (for)

    La estructura for, nos permite iterar numeros o nombre dependiendo de lo que
    se quiera programar, podemos ingresar validaciones de numero que comienze con 1
    y que finalize en 100 y el programa realizara el bucle hasta contar los 100 
    numeros que se le asignaron. finaliza ejecucion luego de la validacion. 

Lectura de sentencia (while)

    La sentencia while nos permite crear un bucle sin fin, de manera que el programa
    compilara las mil veces que querramos hasta donde le pongamos un tope para
    finalizar, caso contrario no se detendra.

Lectura (Function)

    Una funcion es un constructor que nos permite generar una opcion de un menu que solo
    se debe llamar a la funcion ala parte principal y ejecutara todo su contenido 
    tambien en otros casos se le conoce como arreglos.

# Martes

Ejercicio multiplicación

    multiply = function (a, b) {
      return a * b;
    }

Ejercicio Ascii.

    function uniTotal(codigo) {
    let longitud = codigo.length;
    let suma = 0;
    for (let i = 0; i < longitud; i++){
        suma = suma + codigo.charCodeAt(i);
    }
    return suma;
    }

# Miercoles

Ejercicio Char ascii

    function getChar(color){
    return String.fromCharCode(color);
    // fromCharCode, es el llamado a convertir en codigo ascii...
    }

Ejercicio suma Binaria.

    function addBinary(a,b) {

    return (a+b).toString(2);
    console.log(a,b+"\t= tu resultado es: "+a+b)
    }
    //toString dvuelve un valor binario.

Ejercicio Calificación Final del Estudiante.

        function finalGrade (exam, projects) {
    //exam = 91;
    //projects = 11;
    
    let validacion = 0;
    if(exam > 90 || projects >10){
        validacion = 100;
        //console.log("\tEl alumno gano con meritos ")
    }else if(exam > 75 && projects >=5){
        validacion = 90;
        //console.log("\tEl alumno tiene nota aceptable")
    }else if(exam >50 && projects >=2){
        validacion = 75;
        //console.log("\tEl alumno necesita mejorar la nota")
    }else if(exam <50 && projects <2){
        validacion = 0;
        //console.log("\tEl Alumno perdio")
    }
    return validacion/* validacion, palabra creada para indicar por la sentencia
    condicional si el alumno aprueba o no.*/

# jueves

ejercicio eliminar todos los signos de exclamacion al final de la oracion.

    function remove (string) { 
    let remover = '';
    let lastVslidStringPosition = string.length -1;
    /*lastVslidStringPosition accion para separar solo los 
    signos de exclamacion de una palabra o conjunto de 
    caracteres*/
    for (let i = lastVslidStringPosition; i>0; i--){
        /*recorriendo la palabra, para encontrar los signos a 
        retirar de la palabra*/
        if(string [i] !== '!'){
        //instruccion para eliminar el signo cuando lo detecte.
        remover = string.substring(0, i +1);
        break;
        }
    } 