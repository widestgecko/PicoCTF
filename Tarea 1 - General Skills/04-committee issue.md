## Solución

Descomprimir el archivo con unzip, "unzip Challenge.zip"

Moverse a la carpeta drop-in y hacer un ls-la.

Hacer un git init para entrar al repositorio.

con git log ver los repositorios anteriores.

commit 42942c9c605b30100f5d859ef6e172027447c0db (HEAD -> master) Author: picoCTF [ops@picoctf.com](mailto:ops@picoctf.com) Date: Tue Mar 12 00:06:23 2024 +0000

```
remove sensitive info
```

commit b562f0b425907789d11d2fe2793e67592dc6be93 Author: picoCTF [ops@picoctf.com](mailto:ops@picoctf.com) Date: Tue Mar 12 00:06:23 2024 +0000

```
create flag
```

Usar "Git checkout b562f0b425907789d11d2fe2793e67592dc6be93" para restablecer ese commit

Usar "cat message.txt" para obtener la flag.

Flag: "picoCTF{s@n1t1z3_c785c319} "

## Notas Adicionales

Use las pistas para saber que hacer.