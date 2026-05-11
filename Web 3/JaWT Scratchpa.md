# Descripción.

Este reto requiere resolver una vulnerabilidad en un sitio web que utiliza **JSON Web Tokens (JWT)** para gestionar sesiones y autorizaciones. El objetivo es autenticarse como el usuario `admin` para obtener la bandera.

**Pistas:**

1. What is a Cookie? (¿Qué es una Cookie?)
2. Have you heard of JWT? (¿Has oído hablar de JWT?)

# Solución.

1. **Analizar la aplicación**: Al acceder a la URL, se presenta un sitio de bloc de notas. Se intenta iniciar sesión como `admin`, pero la aplicación lo impide directamente.
2. **Identificar la vulnerabilidad: Se inicia sesión con un nombre genérico (ej. `BenduOlo` ) y se utilizan herramientas de desarrollador para examinar las **cookies**. Se encuentra un **JWT** que almacena el nombre de usuario.
3. **Modificar el token**: Se copia el token y se utiliza **jwt.io** para decodificarlo. Se cambia el nombre de usuario de `Carlos` a `admin` en el _payload_.
4. **Firma inválida**: Al intentar usar el token modificado, la aplicación da error porque la **firma** ya no coincide con el nuevo contenido.
5. **Crackear la firma**: Se utiliza la herramienta **John the Ripper** junto con una lista de palabras (`rockyou.txt`) para descubrir la clave secreta utilizada para firmar los tokens. La clave revelada es `ilovepico`.
6. **Obtener bandera**: Se genera un nuevo JWT con el usuario `admin` y se firma correctamente usando la clave descubierta. Al actualizar la cookie con este nuevo token, la aplicación concede acceso como `admin` y muestra la bandera.

**Flag: picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}**.

# Notas Adicionales.
- Los JWTs son vulnerables si se firma con una clave secreta débil o si se permite el algoritmo `none`.
- Es fundamental proteger las claves secretas de firma para evitar la manipulación de tokens.

# Referencias.
[https://youtu.be/oiZk0tIkR48?si=oF4abs3wLiprn5iG](https://youtu.be/oiZk0tIkR48?si=oF4abs3wLiprn5iG)