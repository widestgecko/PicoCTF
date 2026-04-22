# Descripción.

This website can be rendered only by picobrowser, go and catch the flag![http://fickle-tempest.picoctf.net:53108](http://fickle-tempest.picoctf.net:53108)

**Pistas:**

1. You don't need to download a new web browser.

# Solución.

1. Entré al sitio web indicado.
2. Abrí la **consola de desarrollador** con clic derecho y seleccionando "Inspeccionar".
3. Fui a la pestaña **Red (Network)** y recargué la página para ver la petición.
4. Modifiqué el encabezado **User-Agent** en la petición por `picoBrowser`.
5. Al enviar la petición modificada, el servidor me mostró la bandera. **Flag: picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}**

# Referencias.

[https://youtu.be/9d6-N0oJwOk?si=ufCZ6RAUUJyAFVms](https://youtu.be/9d6-N0oJwOk?si=ufCZ6RAUUJyAFVms)