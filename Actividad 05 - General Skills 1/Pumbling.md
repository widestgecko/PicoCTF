# Descripción.

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?Connect to fickle-tempest.picoctf.net 62718.

_**pistas**_

- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This kind
# Solución.

Use las pipas para redireccionar la salida de la conexion y use grep para encontrar la bandera. $ nc fickle-tempest.picoctf.net 62718 | grep -oE "picoCTF{.*?}" picoCTF{digital_plumb3r_1eBfC512}
# Notas Adicionales.

- `-o` (only-matching): Te muestra **solo** el texto que coincide, no toda la línea. Muy útil si la línea mide 10,000 caracteres.
    
- `.*?` : Busca todo lo que haya dentro de los corchetes de forma "perezosa" (se detiene en el primer `}`).