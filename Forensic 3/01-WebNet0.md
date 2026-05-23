## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Solución

Abrir en Wireshark

Ir a Editar > Preferencias > Protocolos > TLS > Lista de claves RSA

Añade la clave a la lista (no te preocupes por la IP ni otras columnas)

La bandera está en la sección TLS descifrada de los paquetes HTTP ahora visibles

picoCTF{nongshim.shrimp.crackers}