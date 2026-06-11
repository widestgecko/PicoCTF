# Descripción.
En este reto se analiza una función que recibe dos argumentos (`0x8` y `0x2e`). El código introduce el uso de variables locales reservando espacio en la pila y contiene un bucle (loop) que incrementa estas variables repetidamente hasta cumplir una condición límite.

# Solución.
1. Se reservan 16 bytes en la pila para variables locales (`sub esp,0x10`).
    
2. Se inicializan dos variables locales: `var1` (`[ebp-0x4]`) con el valor del segundo argumento (`0x2e`) y `var2` (`[ebp-0x8]`) con el valor del primer argumento (`0x8`).
    
3. El flujo salta a la evaluación de la condición del bucle: comprobar si `var2` es menor o igual a `0xe6da`.
    
4. En cada iteración del bucle, `var1` se incrementa en `1` y `var2` se incrementa en `0xed`.
    
5. En lugar de iterar manualmente, se calcula matemáticamente: el bucle necesita cubrir una distancia de `0xe6da - 0x8 = 59090` (decimal) sumando `0xed` (237 decimal) por ciclo. Esto da exactamente 250 iteraciones.
    
6. Se calcula el valor final de `var1`: `46 (0x2e) + 250 = 296`.
    
7. Se convierte el resultado a hexadecimal y se retorna desde el registro `eax`. El resultado es **0x128**. **Flag: 0x128**
    

# Notas Adicionales.
El reto demuestra cómo se estructuran los bucles `while` o `for` a bajo nivel, y destaca la importancia de traducir los bucles repetitivos a matemáticas simples para resolverlos de manera estática y eficiente sin necesidad de ejecutar el código.