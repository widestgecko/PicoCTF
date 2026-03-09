# Descripción.

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too. **Pistas:**

1. To view the file in the webshell, do: `$ nano level1.py`
2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solución.

1. Descargue los archivos.
2. Ejecute el script, me pide una contraseña.
3. abrí el script con nano, para ver si podría encontrar la contraseña.
4. Encontré la contraseña dentro del script, dentro de un if.
5. Ejecute de nuevo el script e ingrese la contraseña y me dio la bandera. **Flag: picoCTF{545h_r1ng1ng_1b2fd683}**