# Descripción.

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

**Pistas:**

1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solución.


1. Descargue los archivos.
2. hice nano al archivo python para ver si podia obtener la bandera.
3. Estaba en formato hexadecimal, asi que traduje en otra ventana la contraseña. $ echo "64653736" | xxd -r -p de76
4. Ejecute de nuevo el script con la contraseña y me dió la bandera. $ python3 level2.py Please enter correct password for flag: de76 Welcome back... your flag, user: picoCTF{tr45h_51ng1ng_489dea9a} **Flag: picoCTF{tr45h_51ng1ng_489dea9a}**