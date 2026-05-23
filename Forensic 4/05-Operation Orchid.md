## Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)

## Solución

Descargar el archivo. Desencriptarlo con gunzip. gunzip disk.flag.img.gz Hacer mmls para ver las particiones. mmls disk.flag.img Listamos las particiones. fls -o 2048 disk.flag.img fls -o 411648 disk.flag.img 472 icat -o 411648 disk.flag.img 1782 strings -t d disk.flag.img | grep flag.txt icat disk.flag.img -o 411648 1782 > flag.txt.enc

Usar openssl para obtener la flag. openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567 cat flag.txt

picoCTF{h4un71ng_p457_1d02081e}