## Descripción
Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:53007/) to find the flag

## Solución

En la pagina abaout me viene el texto "# Try inspecting the page!! You might find it there" por lo que al inspeccionar esa parte viene una cadena de caracteres en base 64.

usando el siguiente comando en linux obtenemos la flag. echo cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9 | base64 -d

picoCTF{web_succ3ssfully_d3c0ded_df0da727}

## Notas Adicionales


Se puede usar la función decoder de burp suite.