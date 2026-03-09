#### Description

Can you convert the number 42 (base 10) to binary (base 2)?

# Solución.

Primero investigue la forma en que se pueden convertir numeros decimales a binario en linux, encontre una pagina donde explican la forma de hacer esta convercion con comandos.

El comando es el siguiente: _echo "obase=2; 42" | bc_ como resultado me dio: 101010

Por lo tanto la bandera es: picoCTF{101010}