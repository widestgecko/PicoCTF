# Descripción.

There's an interesting script in the user's home directoryThe work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

Hostname: saturn.picoctf.net Port: 62359 Username: picoplayer Password: password

# Solución.

1. Me conecte usando ssh y el usuario picoplayer: ssh [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net) -p 62359
2. use la contraseña que se me otorgo en el reto: ![[Screenshot_2026-02-19_21-09-31.png
3. use ls para ver lo que habia y solo estaba un script llamado useless.
4. ejecute el script con ./useless
5. el script dio como resultado un mensaje que decia que lea el codigo primero.
6. hice un cat al useless.
7. observe que mencionaban el manual del programa.
8. ejecute el manual de useless: ![[Pasted image 20260219211457.png]] **Flag: picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_4151}**