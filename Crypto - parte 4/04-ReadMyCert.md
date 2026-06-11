## Descripción
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/423/readmycert.csr).

## Solución

Vemos que una linea esta en base 64 por lo que uso echo cGljb0NURntyZWFkX215Y2VydF81N2Y1ODgzMn0 | base64 -d para obtener la bandera. Bandera: picoCTF{read_mycert_57f58832}