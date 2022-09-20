# week 8.
# Lunes.

Encapsulamiento.
    
    El encapsulamiento dentro de los programas, funciona de manera que no sea manejable por
    alguna otra persona los datos que dentro de eso se almacenan, como pueden ser datos de 
    contraseña de usuario o sueldos, son datos que no cualquiera debe de alterar por esas razón
    la funcionalidad de escapsulamiento priva a que solo el responsable de esos cambios debe entrar
    para poder modificarlos, si no es el nadie más los puede realizar, haciendo al sistema más
    seguro y confiable para el personal que lo opere y evitandose malos intencionados.

Abstracción.

    El metodo de abstracción, nos simplifica más la busqueda de elementos ya que varios de los objetos
    muchas veces tienen los mismo elementos y simplificarlos es de gran ayuda esto es lo que el metodo de
    abstracción genera, porque mediante el proceso que se le atribuye a un objeto nos puede servir para todos
    los demas elementos, ahorrandonos codigo y demás dentro del programa.

Herencia.

    Dentro de la clase principal del programa se puede obtener un padre, asi llamado porque este tiene varias
    propiedades que derivan de ello, al momento de generar otra clase, se puede mandar a llamar un elemento que
    contiene el padre, porque ese elemento que contiene genera la misma funcionalidad para esa clase, sin 
    necesidad de tener codigo de más.
    dentro de otra clase puede acceder a sus metodos que ya se tienen y darles otro uso que a su vez
    tambien implementa ala clase principal.

Polimorfismo.

    Genera el uso de un metodo para varias funciones, esto genera que el codigo este reducido y que trabaje más
    sin necesidad de gastar más recursos.

# Martes.

Diversión con Parametros.

    function addNumbers (x: number, y: number): number {
    return x + y;
    }
    ; // Returns 3
    console.log(addNumbers(1, 2));
    console.log(addNumbers(1,3));    // Returns an error. 

Clases Abstractas.

    Dentro de una clase abstracta no puede ser una instancia, si no que, solo lo hereda, es una
    super clase respecto de otras clases.

Clase Abstracta vrs Interfaz.

    La interfaz es una de las formas de realizar que varias clases se conecten para poder
    interactuar de la mejor manera, mientras que las Clases abstractas son una super clase
    que contienen propiedades que siempre se deben usar en la siguiente clase.

# Miercoles.
Haz, que el pez muerto Nade.

    export function parse(data: string): number[] {
    let v = 0,
        result: number[] = [];
    for (let d of data.split('')) {
        switch (d) {
        case 'i':
            v++;
            break;
        case 'd':
            v--;
            break;
        case 's':
            v *= v;
            break;
        case 'o':
            result.push(v);
        }
    }
    return result;
    }


Código Duplicado.

    Generar un programa capaz de reconocer las letras duplicadas, separandolas y además
    contandolas por aparte.

    export function duplicateEncode(word: string){ // Success
    // lower case
    word = word.toLowerCase(); // 'success'
    // (string) | (string[]) ***
    const characters: string[] = word.split(''); // ['s','u','c','c','e','s','s']
    // iterar 
    const encoded: string[] = characters.map((character) => {
        character = character.replace(/\(/g, '\\(');
        character = character.replace(/\)/g, '\\)');
        const regex = new RegExp(character, 'g');
        const found = word.match(regex) || [];
        if(found.length === 1) {
        return '(';
        } 
        return ')';  
    }); // [')','(',')',')','(',')',')']
    return encoded.join('');  
    }

Número Impar.

    El programa debe de realizar una busqueda dentro del arreglo separando los
    números que son impares de los pares.

    const appereances = (numbers: number[], nToCount: number) => {
    return numbers.filter((n: number) => n === nToCount).length;
    };

    export const findOdd = (xs: number[]): number => {
    const nonRepeatNumbers = new Set(xs);
    for (let n of nonRepeatNumbers) {
        if (appereances(xs, n) % 2 !== 0) return n;
    }
    return -1;
    };

# Jueves.

    interface Identity<T, U> {
        value: T;
        message: U;
    }
    let returnNumber: Identity<number, string> = {
        value: 25,
        message: 'Hello!'
    }
    let returnString: Identity<string, number> = {
        value: 'Hello!',
        message: 25
    }
    console.log(returnNumber);


    /*interface ProcessIdentity<T, U> {
        (value: T, message: U): T;
    }
    function processIdentity<T, U> (value: T, message: U) : T {
        console.log(message);
        return value
    }

    console.log(processIdentity(10,'hola'));*/
