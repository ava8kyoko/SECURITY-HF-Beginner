# Encryption - 1 - Bypassing the Password is One Way to do it. (7)

Reverse engineering is the action of taking something, opening it, and understanding how it works. 
This technique is often used to make no-CD cracks, bypass serial numbers and other activation methods. 
OllyDBG is a tool that can help you do just that. Here is a simple program that can be reverse-engineered.
<br><br>
see the file

## Steps (lazy way)
1. `vim main.c`
2. Change this line `caractere = caracter - (strlen(password) + (secret % 10) + encryptChar);`<br>
like this `caractere = caractere + strlen(password) + (secret % 10) - encryptChar;` <br>
Now, I can decrypte the file, instead of encypte it.
3. `chmod 700 main.c` (Not sure if I did it or not. C'est pour qu'il puisse etre execute)
4. Compile `gcc main.c -o exe`
5. Execute `./exe file.enc file.dec ` (or ./a.out if no -o)

## Flag
- You found a flag! <la74ugb4fka5oe5ej3ktj4m2w6ry9c6m\>
