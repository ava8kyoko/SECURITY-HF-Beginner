# Linux - SSH key (2)

## Steps
1. SSH key -> `cat id_ed25519`
```
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACAObEEtj0jyDz1ztFhoUhXT80cGXoxsS2d9qJFQJsrhKAAAAKBUXEowVFxK
MAAAAAtzc2gtZWQyNTUxOQAAACAObEEtj0jyDz1ztFhoUhXT80cGXoxsS2d9qJFQJsrhKA
AAAEBDGPcVd5a/KYLwetA5bQ8Vj0qF5pX7/+UKkTBC7bW2CA5sQS2PSPIPPXO0WGhSFdPz
RwZejGxLZ32okVAmyuEoAAAAHWNlcmVhbGtpbGxlckBpcC0xNzItMzEtODItMTM3
-----END OPENSSH PRIVATE KEY-----
    
```
2. `ls -la` -> `-rw-r--r--  1 kali kali  419 Jun 11 21:41 id_ed25519`
3. `chmod 700 id_ed25519` because 
```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'id_ed25519' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "id_ed25519": bad permissions
cerealkiller@beginner-linux.hfctf.ca: Permission denied (publickey).
```
so `ls -la` -> `-rwx------  1 kali kali  419 Jun 11 21:41 id_ed25519`
4. `cerealkiller@beginner-linux.hfctf.ca -i /tmp/mozilla_kali0/id_ed25519`
5. `cat flag.txt`

## Flag
`HF-D9641062F62354ABC92EFB2988D78FFC`
