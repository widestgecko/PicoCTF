## Descripción
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/189/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.

## Solución

El mensaje se encuentre en una valla de 4 rieles por lo que me encargo de dividir el mensaje en 4 partes:

"Ta __ _7N6D8D hlg:W3D_H3C31N__387 ef_sHR053F38N43DFD _i33___N6"

Después le doy el formato de Zigzag:

T a _ _ 7 N 6 D 8 D h l g : W 3 D _ H 3 C 3 1 N _ _ 3 8 7 e f _ s H R 0 5 3 F 3 8 N 4 3 D F D _ i 3 3 _ _ _ N 6

Obtenemos: The_flag_is:_WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7 picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7}