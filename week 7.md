# Week 7.
# Lunes.
OOP.
    Abstracción:

    Herencia:

    Polimorfismo:

    Encapsulación:

    Clase
    Objeto:

    Instancia:

    Interfaz:

    Modificadores de acceso:
    
    Constructores
    https://youtu.be/5EGS6lnghYE.





POO. Patito de Goma.

    Uno de los ejercicios muy funcionales dentro del mundo de la programación
    que da grandes resultados de como enteder mejor el código que se esta
    compilando y ayuda mucho a que el programador pueda comprender los errores
    de su programa los cuales son muy dificiles de resolver, teniendo como 
    mejor amigo un patito de ule el cual sera utilizado para poder comentarle
    cada funcion de las lineas de código el cual da como finalidad, que el 
    programador recapitule y que vuelva a comprender mejor el proceso de su
    programa y de esa forma explicandoselo a alguien el mismo programador
    comprendera mejor como manejar la cituación de su programa funcional.

# Martes.


# Miercoles.

Ejercicio, hacer una torre.

    if (nFloors === 1) return ['*'];
    const tower: string[] = [];
    const maxNumber = 2 * nFloors - 1;
    for (let i = 1; i <= nFloors; i++) {
        tower.push(
        `${' '.repeat(nFloors - i)}${'*'.repeat(2 * i - 1)}${' '.repeat(
            nFloors - i
        )}`
        );
    }
    return tower;

