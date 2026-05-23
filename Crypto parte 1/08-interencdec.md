## Descripción

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/1/enc_flag).

## Solución

Al abrir el archivo nos dará una cadena en base 64 así que uso echo para descifrarla. echo YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg== | base64 -d b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ==

Nos regresa otra cadena en base 64: echo d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ== | base64 -d

wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}

La cadena regresada esta cifrada en caesar por lo que uso una pagina para ver las 25 posibilidades siendo en mi caso la posibilidad numero 7

picoCTF{caesar_d3cr9pt3d_ea60e00b}