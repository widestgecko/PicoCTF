#### Description

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

# Solución.
Investigue algun comando en linux que me permita traducir el lenguaje hexadecimal y me dio como resultado lo siguiente:
`echo "48656c6c6f" | xxd -r -p`

- `-r` (reverse): Convierte el volcado hexadecimal a binario/ASCII.
- `-p` (plain): Indica que el formato es "plano" (sin estructura de volcado).
**==*Resultado*==**
'p'
Por lo tanto la bandera es picoCTF{p}