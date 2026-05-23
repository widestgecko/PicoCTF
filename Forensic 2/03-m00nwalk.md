## Descripción


Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

## Slución

Instalar qsstv ejecutar pactl load-module module-null-sink sink_name=virtual-cable Ejecutar pavucontrol Ejecutar qsstv Ejecutar `paplay -d virtual-cable message.wav`para crear la imagen: Descargue el cable de audio virtual.

```
$ pactl list short modules | grep null
25      module-null-sink        sink_name=virtual-cable
$ pactl unload-module 25
```

Obtener la flag: picoCTF{beep_boop_im_in_space}