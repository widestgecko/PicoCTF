## Descripción

Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/70/disk.img.gz)
- Remote machine: `ssh -i key_file -p 53445 ctf-player@saturn.picoctf.net`

## Solución

wget [https://artifacts.picoctf.net/c/71/disk.img.gz](https://artifacts.picoctf.net/c/71/disk.img.gz), gzip -d disk.img.gz, mmls disk.img, fls -o 206848 disk.img, fls -o 206848 disk.img 470, fls -o 206848 disk.img 3916, icat -o 206848 disk.img 2345 > id_rsa, chmod 600 id_rsa, ssh -i id_rsa -p 53445 [ctf-player@saturn.picoctf.net](mailto:ctf-player@saturn.picoctf.net) ls, cat flag.txt

picoCTF{k3y_5l3u7h_b5066e83}