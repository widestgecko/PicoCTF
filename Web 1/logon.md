# Descripción.

The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? [http://fickle-tempest.picoctf.net:61116](http://fickle-tempest.picoctf.net:61116)

**Pistas:**

1. Hmm it doesn't seem to check anyone's password, except for Joe's?

# Solución.


1. Ingrese a la pagina.
2. Probe ingresar al sitio, ingrese pero la bandera estaba oculta.
3. abri el modo desarrollador y busque si habia alguna pista en el codigo.
4. Chequé las cookies del sitio y noté que había un apartado para el tipo de usuario, si era admin o no, el mio decia "False".
5. Con un editor de cookies edite esa parte y la cambie a "True".
6. Recargue la pagina y obtuve la bandera.

**Flag: picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}**

# Notas Adicionales.

Editando las cookies se pueden hacer varias cosas interesantes.

# Referencias.

[https://www.youtube.com/watch?v=P2njyHWhu1U&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=3](https://www.youtube.com/watch?v=P2njyHWhu1U&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=3)