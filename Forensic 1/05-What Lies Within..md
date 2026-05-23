## Descripción

There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

## Solución

- Identificar que la imagen utiliza esteganografía LSB
    
- Extraer los bits menos significativos de cada píxel
    
- Reconstruir los datos ocultos a partir de estos bits
    
- La flag se revela en el proceso de extracción picoCTF{h1d1ng_1n_th3_b1t5}