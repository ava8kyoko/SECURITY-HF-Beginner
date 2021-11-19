# Linux (Viper) - Nmap (7)

## Challenge
On the box, you are allowed to use nmap as another user. What can you do with these new privileges? Are you able to read the secret files from the user's home directory?
<br><br>
Note: use the SSH key from the first Linux challenge to log into the box.

## Steps
1. `ssh nmapuser@beginner-linux.hfctf.ca -i /tmp/mozilla_kali0/id_ed25519`
2. `cat /etc/passwd` to check list of users -> `nmapuser:x:1004:1004::/home/nmapuser:/bin/sh`
3. `cd /home/nmapuser`
4. `ls -la` and `cat flag.txt` -> `-r--------  1 nmapuser root       36 Jun 14  2019 flag.txt`
5. I THING I NEED TO DO THE ROOT CHALLENGE BEFORE, because I need the root password

## Flag
``
