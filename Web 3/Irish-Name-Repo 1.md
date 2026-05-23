# Descripción.


picoCTF 2019 - Web - Irish-Name-Repo 1. Este reto de inyección SQL requiere acceder a un sitio web de login y autenticarse sin conocer las credenciales.

**Pistas:**

1. Seems like a lot of ways to interact with this web. I wonder if users are kept in a database?
2. Try to think about how the website verifies your login.

# Solución.


1. **Analizar el sitio**: Al ingresar a la URL, se observa una página simple de lista de nombres. Se examina el código fuente y se identifica un menú que lleva a la página de login (`login.php`).
2. **Identificar vulnerabilidad**: En la sección de soporte del sitio, se observa un error SQL al intentar ingresar nombres, lo que sugiere una vulnerabilidad de **SQL Injection**.
3. **Analizar formulario**: Se examina el formulario de login y se descubre un campo oculto llamado `debug`. Al activar este campo cambiando su valor a `1`, el sitio revela la consulta SQL que se ejecuta en el servidor: `SELECT * FROM users WHERE name='[username]' AND password='[password]'`.
4. **SQL Injection - Login**: Se intenta un login estándar fallido. Luego, en el campo de contraseña, se introduce una carga útil SQL: `' OR 1=1; --`. Esta inyección hace que la condición `WHERE` sea siempre verdadera (`1=1`) y comenta el resto de la consulta con `--`, permitiendo el acceso.
5. **Obtener bandera**: Al enviar el formulario con la inyección en el campo de contraseña, el sitio web muestra la bandera correcta.
6. **Solución alternativa (Consola)**: Se muestra cómo realizar el mismo ataque utilizando `curl` en la terminal, enviando un método `POST` con los parámetros `username`, `password` (con la inyección) y `debug=1`.

**Flag: picoCTF{s0m3_SQL_85832275}**
# Referencias.
[https://youtu.be/0EDbUSDqrng?si=Dtq9P7F7eNTWYmOD](https://youtu.be/0EDbUSDqrng?si=Dtq9P7F7eNTWYmOD)