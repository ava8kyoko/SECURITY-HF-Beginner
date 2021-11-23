2 - The Real Password is Actually a Flag. 8

Reverse engineering is the action of taking something, opening it, and understanding how it works. 
This technique is often used to make no-CD cracks, bypass serial numbers and other activation methods. 
OllyDBG is a tool that can help you do just that. Here is a simple program that can be reverse-engineered.

(Use file from Flag #1)


 A totally legit spreadsheet. 8

This spreadsheet consists of a single macro that, when executed, prints the flag. 
However, this macro is protected with a password. Can you go around it?


 1 - Write your own decryption algorithm.
8

This is a simple Linux encryption algorithm. It has two basic functions: [./encrypt SOURCE DESTINATION] will prompt you for a password to encrypt the file. [./encrypt SOURCE DESTINATION QUICK] will use a hard-coded default password. Flag #1 uses the quick method, so the algorithm can be reversed engineered quite easily. Flag #2 uses the other method, so it will have to be brute forced using the rocksmall.txt word list and a custom script you wrote.




 2 - Homemade bruteforce
10

This is a simple Linux encryption algorithm. It has two basic functions: [./encrypt SOURCE DESTINATION] will prompt you for a password to encrypt the file. [./encrypt SOURCE DESTINATION QUICK] will use a hard-coded default password. Flag #1 uses the quick method, so the algorithm can be reversed engineered quite easily. Flag #2 uses the other method, so it will have to be brute forced using the rocksmall.txt word list and a custom script you wrote.

Use the algorithm your made during Flag #1 and script a bruteforce with rocksmall.txt.

The content of the file looks like this: You found a flag! <[MD5]>