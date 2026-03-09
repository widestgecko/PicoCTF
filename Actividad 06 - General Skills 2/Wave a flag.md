# Descripción.

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information... **Pistas:**

- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget URL here, where the url can be found in the details section.
- Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.

# Solución.

1. Descargue el archivo que venia en la descripcion del reto.
2. Leí las pistas y las ejecute paso a paso.
    1. Ejecute chmod +x warm dentro de la carpeta donde se encontraba el archivo.
    2. Ejecute ./warm y el programa corrió.
3. El mensaje del archivo fue el siguiente: "Hello user! Pass me a -h to learn what I can do!"
4. Ejecute lo que me pedía el programa(./warm -h) y obtuve el siguiente mensaje: "Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}"

**Flag: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}**