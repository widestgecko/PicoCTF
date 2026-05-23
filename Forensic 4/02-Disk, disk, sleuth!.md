## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/a734f18939e0aaea9d27bc7a243a0ed0/dds1-alpine.flag.img.gz)

	## Solución

Descargar el archivo. Descomprimirlo con gzip. Obtener la flag con strings *.img | grep pico

picoCTF{f0r3ns1c4t0r_n30phyt3_a69a712c}