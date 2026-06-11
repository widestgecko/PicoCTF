## Descripción

How to automate tasks to run at intervals on linux servers? Use ssh to connect to this server: Server: saturn.picoctf.net Port: 54013 Username: picoplayer Password: 5wf1w1hVxt

## Solución 

Conectarse al servidor con: ssh -p 54013 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)

Una vez dentro del servidor hacer un cat /etc/crontab para ver la flag.

flag: picoCTF{Sch3DUL7NG_T45K3_L1NUX_9d5cb744}