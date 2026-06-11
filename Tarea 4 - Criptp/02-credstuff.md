## Descripción

We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

## Solución

Abrir el archivo usename.txt con vim y buscar en que linea esta cultiris el cual esta en la linea 378 Usar el comando 'cat passwords.txt| head -n 378 | tail -n 1' Obtenemos la siguiente cadena en rot13: cvpbPGS{P7e1S_54I35_71Z3} Usar echo cvpbPGS{P7e1S_54I35_71Z3} | rot13 Nos dara la bandera. bandera: picoCTF{C7r1F_54V35_71M3}