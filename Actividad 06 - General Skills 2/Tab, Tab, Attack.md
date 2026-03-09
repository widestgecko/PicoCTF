
# Descripción.

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames. **Pistas:** After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

# Solución.

1. Descargue el archivo comprimido.
2. Descomprimí el archivo y me dio una carpeta, hice un cd a esa carpeta presionando tab todas las veces posible para ir hasta la raíz.  
    $ unzip Addadshashanammu.zip Archive: Addadshashanammu.zip creating: Addadshashanammu/ creating: Addadshashanammu/Almurbalarammi/ creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/ creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/ creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/ creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/ creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/ extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet

$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/

1. el archivo que estaba era un binario, por lo que use strings y un grep para obtener la bandera. $ ls fang-of-haynekhtnamet fang-of-haynekhtnamet.c

$ strings fang-of-haynekhtnamet | grep "picoCTF{" _ZAP!_ picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

**Flag: picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}**