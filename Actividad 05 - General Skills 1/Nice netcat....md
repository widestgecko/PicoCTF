# Descripción.

There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 63484, but it doesn't speak English... **Pistas**

- You can practice using netcat with this picoGym problem: what's a netcat?
- You can practice reading and writing ASCII with this picoGym problem: Let's Warm Up

# Solución.

me conecte y redirigi la salida a un archivo txt para posteriormente procesarlo con python para transformarlo de ascci a texto:

$ nc wily-courier.picoctf.net 63484 >>> flagNiceCat.txt

$ cat flagNiceCat.txt | python3 -c "import sys; print(''.join([chr(int(n)) for n in sys.stdin.read().split()]))"r(int(n)) for n in sys.stdin.read().split()]))"

**==Flag:==** picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}

# Notas Adicionales.

un codio assci normalmente se logra identificar por usar únicamente numeros y por lo general suelen ser grandes.