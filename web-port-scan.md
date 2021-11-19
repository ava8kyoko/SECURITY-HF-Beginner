# Web (Viper) - Port scan (3)

## Challenge
By default, nmap will only scan the top 1000 ports. Can you learn how to fix this? If you find a weird port, you can poke it with nc (netcat).
<br>
The wanted port is within the 13XXX.
<br>
Address: beginner-web.hfctf.ca
<br>
Recommended Tools: nmap, nc (netcat)

## Steps
1. `nmap -p 0-14000 beginner-web.hfctf.ca` -> `13337/tcp open  unknown`
2. `nc beginner-web.hfctf.ca 13337`

## Flag
`HF-6DA40A2D1CBA006ABAC5663543B69994`
