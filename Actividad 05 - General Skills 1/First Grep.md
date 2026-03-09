
# Solución.

Primero busque un pequeño tutorial para usar grep, despues aplique lo visto: $ grep -oE "picoCTF{.*?}" file picoCTF{grep_is_good_to_find_things_9C6Ef2F7}

# Notas Adicionales.

`grep -oE "picoCTF{.*?}" archivo`

- `-o` (only-matching): Te muestra **solo** el texto que coincide, no toda la línea. Muy útil si la línea mide 10,000 caracteres.
    
- `.*?` : Busca todo lo que haya dentro de los corchetes de forma "perezosa" (se detiene en el primer `}`).