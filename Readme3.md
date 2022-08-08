# 3 Weeks
# Lunes

Primer Ejercicio    A quien le gusta?.

    function likes(names) {
    if (names.length == 0) return 'no one likes this';
    if (names.length == 1) return `${names[0]} likes this`;
    if (names.length == 2) return `${names[0]} and ${names[1]} like this`;
    if (names.length == 3)
        return `${names[0]}, ${names[1]} and ${names[2]} like this`;
    return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
    }

Ejercicio Conteo de bits

    var countBits = function(n) {
      // Program Mevar countBits = function (n) {
      let binaryNumber = n.toString(2);
      let oneBitCount = 0;
      for (let i = 0; i < binaryNumber.length; i++) {
        if (binaryNumber[i] === '1') oneBitCount++;
      }
      return oneBitCount;
    };

Ejercicio su pedido.

    function getWordNumber(word) {
      for (let i = 0; i < word.length; i++) {
        if (!Number.isNaN(Number(word[i]))) return word[i];
      }
    }

    function cleanUndefined(array) {
      let result = [];
      for (let i = 0; i < array.length; i++) {
        if (array[i] != undefined) result.push(array[i]);
      }
      return result;
    }

    function order(words) {
      let sortedArray = [];
      let wordsArray = words.split(' ');
      for (let i = 0; i < wordsArray.length; i++) {
        let wordNumber = getWordNumber(wordsArray[i]);
        sortedArray[wordNumber] = wordsArray[i];
      }
      return cleanUndefined(sortedArray).join(' ');
    }
    
 # Martes
 Ejercicio latin de cerdo simple.
 Mueva la primera letra de cada palabra al final de la misma, luego agregue "ay" al final de la palabra. Deje los signos de puntuación intactos.
 
     function pigIt(str) {
      let pMarks = ['!', '¡', '?', '¿', '.', ',', ':', ';'];
      str = str.split(' ');
      for (let i = 0; i < str.length; i++) {
        if (pMarks.indexOf(str[i]) >= 0) continue;
        str[i] = str[i].slice(1) + str[i].slice(0, 1) + 'ay';
      }
      return str.join(' ');
    }
    
  Cuente el número de duplicados
Escriba una función que devuelva el recuento de caracteres alfabéticos y dígitos numéricos distintos que no distinguen entre mayúsculas y minúsculas que aparecen más de una vez en la cadena de entrada. Se puede suponer que la cadena de entrada contiene solo letras (tanto mayúsculas como minúsculas) y dígitos numéricos.

    function duplicateCount(text) {
      let textArray = text.toLowerCase().split('').sort();
      let i = 0,
        result = 0,
        lastIndexOfChar = 0;
      while (textArray.length) {
        lastIndexOfChar = textArray.lastIndexOf(textArray[i]);
        if (lastIndexOfChar !== i) {
          i = lastIndexOfChar;
          result++;
        }
        textArray = textArray.slice(++i);
        i = 0;
      }
      return result;
    }

Ejercicio Codigo Morse.

    decodeMorse = function (morseCode) {
      morseCode = morseCode.replace(/   /g, '#');
      let decodedCode = '';
      let tempWordToDecode = '';
      for (let i = 0, lenght = morseCode.length; i < lenght; i++) {
        if (morseCode[i] === ' ') {
          decodedCode += MORSE_CODE[tempWordToDecode] || '';
          tempWordToDecode = '';
        } else if (morseCode[i] === '#') {
          decodedCode += `${MORSE_CODE[tempWordToDecode] || ''} `;
          tempWordToDecode = '';
        } else {
          tempWordToDecode += morseCode[i];
        }
      }
      decodedCode += MORSE_CODE[tempWordToDecode] || '';
      return decodedCode.trim();
    };
    
  # Miercoles.
  Escribe una función que tome una cadena de paréntesis y determine si el orden de los paréntesis es válido. La función debería regresar truesi la cadena es válida y false si no es válida.
  
     function validParentheses(parens) {
      let valid = 0;
      for (let i = 0; i < parens.length; i++) {
        if (parens[i] === ')') valid--;
        if (parens[i] === '(') valid++;
        if (valid < 0) return false;
      }
      return valid == 0;
    }
 
Ejercicio. 
Complete el método/función para que convierta las palabras delimitadas por guiones/guiones bajos en mayúsculas y minúsculas. La primera palabra dentro de la salida debe estar en mayúsculas solo si la palabra original estaba en mayúsculas (conocido como Upper Camel Case, también conocido como caso Pascal).

    function toCamelCase(str) {
      let result = '';
      for (let i = 0; i < str.length; i++) {
        if (i != 0 && (str[i - 1] === '_' || str[i - 1] === '-')) {
          result += str[i].toUpperCase();
        } else if (str[i] != '-' && str[i] != '_') {
          result += str[i];
        }
      }
      return result;
    }

ejercicio unico en orden.
Implemente la función unique_in_order que toma como argumento una secuencia y devuelve una lista de elementos sin ningún elemento con el mismo valor uno al lado del otro y conservando el orden original de los elementos.

    function uniqueInOrder(iterable) {
      let result = [];
      let last;
      for (let i = 0; i < iterable.length; i++) {
        if (iterable[i] !== last) {
          last = iterable[i];
          result.push(last);
        }
      }
      return result;
    }

# jueves
Ejercicio doblar una matriz.

    function foldArray(array, runs) {
      if (array.length === 1) return array;
      let output = [...array];
      let aheadPosition = 0;
      while (runs) {
        if (output.length === 1) return output;
        output = Array.from(
          { length: Math.round(output.length / 2) },
          (v) => 0
        ).map((v, i) => {
          aheadPosition = output.length - (i + 1);
          if (aheadPosition === i) return output[i];
          return output[i] + output[aheadPosition];
        });
        runs--;
      }
      return output;
    }
    
ejercicio cifrar esto.

    function encryptedWord(word) {
      if (word.length == 1) return word.charCodeAt();
      if (word.length == 2) return `${word.charCodeAt(0)}${word[1]}`;
      return `${word.charCodeAt(0)}${word[word.length - 1]}${word.slice(
        2,
        word.length - 1
      )}${word[1]}`;
    }

    var encryptThis = function (text) {
      return text.split(' ').map(encryptedWord).join(' ');
    };
    
# Desafia Principal.
Quien eres?

    Una persona dispuesta a entender nuevos retos,tratando de comprender lenguajes de programación
    que me impulsaran en un futuro a largo plazo.
    Buscando una superación personal y trabajar en codigo, es complicado y requiere mucha logica
    pero, siempre es entretenido en lo personal es la razon del porque me gusta la programación.
    
