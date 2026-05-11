# Descripción.

Este reto requiere resolver una vulnerabilidad de **SQL Injection (SQLi)** en un sitio web que utiliza una base de datos **SQLite** para gestionar usuarios y datos. El objetivo es explotar la vulnerabilidad para autenticarse como `admin` y eventualmente obtener la bandera oculta en la base de datos.

**Pistas:**

1. Examina las consultas SQL realizadas por la aplicación.
2. Considera cómo un comentario SQL puede afectar la consulta.

# Solución.

1. **Analizar la aplicación**: Al acceder a la web, se presenta un formulario de inicio de sesión. Se intenta un inicio de sesión genérico para entender cómo la aplicación maneja los datos.
2. **Identificar la vulnerabilidad**: Se descubre que el campo de contraseña es vulnerable a inyección SQL. Al ingresar `'or 1=1;--` en el campo de contraseña, se logra omitir la autenticación y acceder como usuario.
3. **Explorar la base de datos**: Una vez dentro, se utiliza una técnica de `UNION SELECT` para consultar la tabla `sqlite_master` y obtener la estructura de la base de datos, revelando la existencia de una tabla llamada `more_table`.
4. **Obtener la bandera**: Se realiza otra inyección `UNION SELECT` para extraer el contenido de la columna `flag` desde la tabla `more_table`.

**Flag: picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_e3e46aae}**

# Notas Adicionales.

- Las vulnerabilidades de inyección SQL ocurren cuando la entrada del usuario no se desinfecta adecuadamente antes de incluirla en una consulta.
- El uso de herramientas de desarrollador o proxies puede ayudar a analizar las peticiones y respuestas.

# Referencias.

[https://youtu.be/W1EjP6OFpUQ?si=4zWPcb5niX0LsyMl](https://youtu.be/W1EjP6OFpUQ?si=4zWPcb5niX0LsyMl)