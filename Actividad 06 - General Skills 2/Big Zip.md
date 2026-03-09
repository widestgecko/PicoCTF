# Descripción.


Unzip this archive and find the flag. **Pistas:** Can grep be instructed to look at every file in a directory and its subdirectories?

# Solución.

1. Descargue el archivo.
2. Descomprimi el archivo.

3. Al ver que eran muchisimos archivos y carpetas, no era eficiente usar grep de una manera normal archivo por archivo, por lo que use grep -r para que lo haga recursivamente en todas las carpetas y archivos para encontrar la bandera. $ grep -r "picoCTF{" big-zip-files big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

**Flag: picoCTF{gr3p_15_m4g1c_ef8790dc}**