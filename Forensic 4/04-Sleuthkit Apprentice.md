## Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)

## Solución

Descargar el archivo. Descomprimir con gzip. Usar los siguientes comandos: mmls disk.flag.img fls disk.flag.img -o 0000360448 fls disk.flag.img -o 0000360448 -r | grep flag icat disk.flag.img -o 360448 2371 picoCTF{by73_5urf3r_2f22df38}