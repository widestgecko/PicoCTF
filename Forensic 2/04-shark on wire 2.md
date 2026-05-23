## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución

usar udp.port == 22 . Se observa que todos tienen 5XXX por lo que esos 3 valores son caracteres hexadecimales que hay que convertir a ascii. 112 p 105 i 99 c 111 o 67 C 84 T 70 F 123 { 112 p 49 1 76 L 76 L 102 f 51 3 114 r 51 3 100 d 95 _ 100 d 97 a 116 t 97 a 95 _ 118 v 49 1 97 a 95 _ 115 s 116 t 51 3 103 g 48 0 125 }

Juntar todas las letras y obtener la key. picoCTF{p1LLf3r3d_data_v1a_st3g0}