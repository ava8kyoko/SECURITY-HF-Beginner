# LM (5)

## Challenge
LM hashes were used by Microsoft for password storage and is now replaced by NTLM. Can you crack this hash?
<br>
0182BD0BD4444BF83535BADF93F05C79
<br>
Recommended tools: 
- hashid : <a href="https://github.com/psypanda/hashID">GitHub</a>
- john : a tool to find weak passwords of your users
- hashcat : Advanced CPU-based password recovery utility
<br>
Recommended <a href="https://en.wikipedia.org/wiki/LAN_Manager">read</a>

## Pre-steps
Make sure that the rockyou.txt is extracted
1. `cd /usr/share/wordlist`
2. `file rockyou.txt.gz`
```rockyou.txt.gz: gzip compressed data, 
last modified: Wed Jul 17 09:59:21 2019, 
from Unix, original size modulo 2^32 139921507
```

3. `sudo gzip -d rockyou.txt.gz`
4. `ls` -> rockyou.txt

## Steps
1. `echo "0182BD0BD4444BF83535BADF93F05C79" >> hash_LM`
2. `hashcat -a 0 -m 3000 hash_LM.txt /usr/share/wordlists/rockyou.txt`
```
Host memory required for this attack: 64 MB

Dictionary cache built:
* Filename..: /usr/share/wordlists/rockyou.txt
* Passwords.: 27181943
* Bytes.....: 139921507
* Keyspace..: 27181943
* Runtime...: 4 secs

0182bd0bd4444bf8:1234567                         
3535badf93f05c79:891011                          
                                                 
Session..........: hashcat
Status...........: Cracked
Hash.Name........: LM
Hash.Target......: hash_LM.txt
Time.Started.....: Sun Nov 21 17:15:44 2021 (0 secs)
Time.Estimated...: Sun Nov 21 17:15:44 2021 (0 secs)
Guess.Base.......: File (/usr/share/wordlists/rockyou.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:   263.8 kH/s (3.11ms) @ Accel:1024 Loops:1 Thr:1 Vec:8
Recovered........: 2/2 (100.00%) Digests
Progress.........: 20480/27181943 (0.08%)
Rejected.........: 0/20480 (0.00%)
Restore.Point....: 18432/27181943 (0.07%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidates.#1....: CESS -> Y
```

## Flag
`1234567891011`
