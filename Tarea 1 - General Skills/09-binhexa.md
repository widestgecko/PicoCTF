## Descripción
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 62766`

## Solución

Conectarse al servidor "`nc titan.picoctf.net 62766`"

Convertir los números decimales: 11000111 = 199 10001110 = 142

Hacer la operación ' | ' para obtener el resultado "11001111"

Hacer la operación " & " para obtener "10000110"

Hacer operación '+ ' para obtener " 101010101 "

Hacer operación ' * ' hacer la multiplicación y obtener el resultado "110111001100010"

Hacer operación '<<' para desplazar el numero binario 1 a la izquierda.

11000111 << 10001110 para obtener "11000111"

Hacer operación '>>' para desplazar el numero binario 2 a la derecha.

```
10001110 >> 1 = 01000111 para obtener " 01000111 "
```

Por ultimo convertir 01000111 a Hexadecimal: 01000111 = 71 = 0x47

## Notas Adicionales

## Referencias
[https://www.prepostseo.com/tool/decimal-to-binary-converter](https://www.prepostseo.com/tool/decimal-to-binary-converter)