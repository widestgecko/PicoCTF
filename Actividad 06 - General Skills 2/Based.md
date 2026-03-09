# Descripción.

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?Connect with nc fickle-tempest.picoctf.net 52311. **Pistas**

- I hear python can convert things.
- It might help to have multiple windows open.

# Solución.

me conecte con nc, me dieron las palabras codificadas en diferentes bases, use gemini para que me ayudara a decifrar las palabras, posteriormente me dieron la bandera.

$ nc fickle-tempest.picoctf.net 52311 Let us see how data is stored chair Please give the 01100011 01101000 01100001 01101001 01110010 as a word. ... you have 45 seconds.....

Input: chair Please give me the o143 o157 o154 o157 o162 o141 o144 o157 as a word. Input: colorado Please give me the 74657374 as a word. Input: test You've beaten the challenge Flag: picoCTF{learning_about_converting_values_bf1F59A2}

**==Flag:==** picoCTF{learning_about_converting_values_bf1F59A2}