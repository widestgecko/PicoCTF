## Descripción
## Solución
Empiezo por escribir "/secret/" al final de la url. Inspecciono el codigo fuente y veo que hay un archivo "hidden/file.ccs" el cual al dar clic muestra una pagina en blanco. agrego "hidden/" al final de url. Me envia a otra pagina en la que inspecciono el codigo fuente y veo el archivo "superhidden/file.css", agrego "superhidden/" a la url.

Sale una pagina con el texto "# Finally. You found me. But can you see me" por lo que inspecciono el codigo fuente y ahí se encuentra la flag.

picoCTF{succ3ss_@h3n1c@10n_790d2615}