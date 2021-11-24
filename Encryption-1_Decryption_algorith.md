Encryption - 1 - Write your own decryption algorithm. (8)

This is a simple Linux encryption algorithm. <br>
It has two basic functions: [./encrypt SOURCE DESTINATION] will prompt you 
for a password to encrypt the file. 
[./encrypt SOURCE DESTINATION QUICK] will use a hard-coded default password. 
Flag #1 uses the quick method, so the algorithm can be reversed engineered 
quite easily. Flag #2 uses the other method, so it will have to be brute forced 
using the rocksmall.txt word list and a custom script you wrote.

## Steps (FLAG #1)
1. `vim main.c`
2. Change this line `caractere = caracter - (strlen(password) + (secret % 10) + encryptChar);`<br>
like this `caractere = caractere + strlen(password) + (sec4ret % 10) - encryptChar;` <br>
Now, I can decrypte the file, instead of encypte it.
3. `chmod 700 main.c` (Not sure if I did it or not. C'est pour qu'il puisse etre execute)
4. Compile `gcc main.c -o exe`
5. Execute `./exe file.enc file.dec ` (or ./a.out if no -o)

## Flag
- You found a flag! <la74ugb4fka5oe5ej3ktj4m2w6ry9c6m\>

## Steps (FLAG #2)

```
import os

with open("rocksmall.txt", "r") as file:
  for line in file:
    payload ="./main flag.txt.enc crack/file" + line.strip() + " " + line.strip()
      print (payload)
      stream = os.popen(payload)
      output = stream.read()
      print(output)
```

## Flag

