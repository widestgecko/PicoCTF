# Descripción.
Este desafío requiere evaluar una función con tres argumentos hexadecimales de 32 bits (`0xb75a8f13`, `0xe1860bd7`, `0xc8e62f81`). La complejidad radica en que el código no lee los argumentos completos, sino que extrae bytes (`BYTE PTR`) y palabras de 16 bits (`WORD PTR`) específicos directamente de la memoria, realizando operaciones a nivel de bits en sub-registros (`eax`, `ax`, `ah`, `al`).

# Solución.

1. Se mapean los argumentos en la pila teniendo en cuenta la arquitectura _Little Endian_ (los bytes menos significativos se guardan primero en memoria).
    
2. Se limpia el registro `eax` (`xor eax,eax`).
    
3. Se mueve el byte en `[ebp+0x9]` (que es `0x8f`) al registro `ah`. (`eax = 0x00008f00`).
    
4. Se desplaza `ax` a la izquierda 16 posiciones (`shl ax,0x10`). Como `ax` solo tiene 16 bits, esto vacía el registro llenándolo de ceros (`eax = 0x00000000`).
    
5. Se resta el byte en `[ebp+0xf]` (`0xe1`) al registro `al` (`0x00 - 0xe1`), lo que produce un _underflow_ resultando en `0x1f`. (`eax = 0x0000001f`).
    
6. Se suma el byte en `[ebp+0xd]` (`0x0b`) al registro `ah` (`0x00 + 0x0b = 0x0b`). (`eax = 0x00000b1f`).
    
7. Se realiza un XOR entre `ax` (`0x0b1f`) y el _Word_ en `[ebp+0x12]`. Por Little Endian, los bytes `e6` y `c8` se leen como `0xc8e6`. El resultado de `0x0b1f ^ 0xc8e6` es `0xc3f9`.
    
8. El valor contenido en `eax` se retorna. El resultado es **0xc3f9**. **Flag: 0xc3f9**
    

# Notas Adicionales.

Este es el reto más técnico de los tres. Exige un entendimiento profundo del formato _Little Endian_ para lectura de memoria y del solapamiento arquitectónico de los registros de propósito general en x86 (cómo modificar `ah` o `al` afecta directamente el valor de `eax`). Además, repasa operaciones aritméticas con desbordamientos (_underflow_) y operaciones lógicas a nivel de bits (_shift_ y _XOR_).