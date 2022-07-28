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