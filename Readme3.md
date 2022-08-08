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
