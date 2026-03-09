# Descripción.

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `57735`.

**Pistas:** Finding a cheatsheet for bash would be really helpful!

# Solución.

1. Me conecte a la instancia.
2. Hice ls e hice un cat al archivo con una parte de la bandera, despues hice lo mismo con las instrucciones de la siguiente parte.
3. hice un "cd /" y me llevo a la siguiente parte de la bandera junto con las instrucciones para encontrar la ultima parte de la bandera.
4. hice de nuevo "cd /" y encontre la ultima parte de la bandera y solo las junte. **Flag: picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}**