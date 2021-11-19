# Linus (Viper) - Sudo (4)

## Challenge
The user cerealkiller has some sudo privileges. Learn to use sudo to be able to read the flag in the user "phantom" home directory.
<br><br>
Requirement: You need to have done the SSH Challenge first Recommendation: Read on sudo

## Steps
1. `cd /home/phantom`
2. `sudo -u phantom cat flag.txt` (-u is to connect as another user)

## Flag
`HF-37C24811BDAC007720BB8FF868386C0F`
