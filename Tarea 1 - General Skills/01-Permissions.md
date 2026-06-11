## Descripción

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 63457 picoplayer@saturn.picoctf.net`Password: `e3pn6lmvHt`Can you login and read the root file?


Conectarse al servidor: ssh -p 63457 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net) Después revisar los permisos de picoplayer con: sudo -vi Empezar a hacer un test de vi e ingresar el comando :!/bin/bash para encontrar la ubicacion de root. Hacer un LS .flag.txt para conocer la flag. picoCTF{uS1ng_v1m_3dit0r_f6ad392b}