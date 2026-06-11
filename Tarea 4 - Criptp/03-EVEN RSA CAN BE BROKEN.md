## Descripción

This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 61554`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/32d7f9da267fbc80629d78138372a9bdf1b8e574080294e184f95878950065d2/encrypt.py).

## Solución

Nos regresa 3 valores los cuales son; N: 16800148920488101446502902870266350262475307371984734840442110170755016935654640474961721263107029922142899142483586666078307110776185896155028426502721438 e: 65537 cyphertext: 6198085543571765939405618826291633572519990684866925422818158050589843989111871189722943360380244419091835478149136233630727535983696659757376755103625717

Estos 3 valores los ingreso en una pagina usando ciphertext como el valor de C:

me regresa la bandera: picoCTF{tw0_1$_pr!m3de643ad5}