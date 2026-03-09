# Descripción.

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 51915` _**pistas**_

- ASCII is one of the most common encodings used in programming.
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

# Solución.

Primero investigue como ejecutar python desde terminal y despues me conecte usando nc, al entrar me dieron la bandera en formato ascci, ejecutable en python, asi que copie la bandera y ejecute un print directo con python3 -c.

$ nc saturn.picoctf.net 51915 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'

$ python3 -c "print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}')" picoCTF{gl17ch_m3_n07_9c42a45d}

**==Flag:==** picoCTF{gl17ch_m3_n07_9c42a45d}