## Descripción

We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Solución

Use el siguiente codigo para calcular el modulo 37. def decode(number):     r = number % 37     return r

def main():     f = open("message.txt", "r", encoding="UTF-8")     lst = f.read().split()   # print(lst[0])

    dec_lst = [] for i in range(len(lst)):         dec_lst.append(decode(int(lst[i])))

```
print(dec_lst)
```

|if **name** == '**main**':     main()    Me regreso: [17, 26, 20, 13, 3, 36, 13, 36, 17, 26, 20, 13, 3, 36, 0, 3, 3, 27, 33, 4, 2, 28]    Usando el mapeo de mod 37 lo convierto a : R0UND_N_R0UND_ADD17EC2    picoCTF{R0UND_N_R0UND_ADD17EC2}