# core-code-from-scratch-readme
# Martes
Mi explicacion aserca de la compilacion e interpretacion.

    Algunos lenguajes de maquina antiguos se crearon con la funcionalidad de interpretar directamente el 
    codigo hacia la maquina  con  el pasar del tiempo otros usuarios de la misma, para facilitar el uso de
    los lenguajes hacia el usuario
    tradujeron la interpretacion a compilacion para que sea mas entendible su funcionalidad para el 
    programador, ahorrandose tiempo al programar.

¿Java está compilado o interpretado, o ambos?
    
    java tiene ambos, porque cuando lo compila lo traslada a codigo intermedio
    que luego se interpreta a codigo de maquina.

Conversor de Divisas.
 
    Pasos
    *Comenzamos pidiendo al usuario sus datos (" ").
    *luego pedimos la cantidad de dolares que el usuario ingresara ("")
    *creamos una conversion de dolares a cantidad bitcoin ("$/b$")
    *mostramos el resultado de cantidad de bitcoins que compro 
     por la cantidad de dolares que aporto.
    *finalizamos mostrando su recibo.

Codigo de Alto y Bajo nivel.
    
    Un codigo de Alto nivel: es el que utiliza diveros medios para traducir el lenguaje maquina
    a sentencias de programación,
    para que sea mas facil de programar al momento de comenzar a hechar codigo.
    El codigo de bajo nivel: es el que se utiliza directamente desde la maquina con unos y seros
    no necesita de un traductor o compilador es un poco más complicado pero gasta menos recursos del sistema.

# Miercoles

Fecha de nacimiento en la Matriz.

    # 1998 = (11111001110);


* Crear un programa que agregue dos números proporcionados por el usuario
* Crea un programa que muestre tu nombre

  .data
        welcome: .asciiz "\n================= Welcome =================\n"
        result: .asciiz "\n Programa suma de dor numeros : "
        number_one_msg: .asciiz "\nIngrese primer numero: "
        number_two_msg: .asciiz "\nIngrese segundo numero: "
	my_name: .asciiz "\n\tRicardo\n"
  .text
        main:
              # welcome message
              li $v0, 4
              la $a0, welcome
              syscall

              # user input
              li $v0, 4
              la $a0, number_one_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t0, $v0

              # user input
              li $v0, 4
              la $a0, number_two_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t1, $v0

              # adding the user numbers
              add $t2, $t0, $t1

              # showing result number
              li $v0, 4
              la $a0, result
              syscall

              # printing number
              li $v0, 1
              move $a0, $t2
              syscall
         

            li $v0, 4
            la $a0, my_name
            syscall



# Jueves 
  Inprecion de numeros Iterativos pares del (0 al 100)

    var i = 0;
    while (i <= 100) {
      if (i % 2 == 0) console.log(i);
      i++;
    }if(i=100){
    console.log("numero especial");
    }