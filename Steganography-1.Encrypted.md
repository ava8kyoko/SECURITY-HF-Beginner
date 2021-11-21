 # Steganography - 1 - Encrypted (5)

## Challenge
This simple file contains 3 flags. Can you dig deep enough?
```
01100001 01010110 01100101 01110010 
01111001 01010011 01110100 01110010 
01101111 01101110 01100111 01010000 
01100001 01110011 01110011 01110000 
01101000 01110010 01100001 01110011 
01100101
```
Check folder inside CTF-HF-2021

## Steps
1. <a href="https://www.rapidtables.com/convert/number/binary-to-ascii.html">Convert binary to ascii</a> -> `aVeryStrongPassphrase`
2. `file FILE.zip.gpg` 
```FILE.zip.gpg: GPG symmetrically encrypted data (AES cipher)```
3. `gpg -d  FILE.zip.gpg`
```gpg: keybox '/home/kali/.gnupg/pubring.kbx' created
gpg: AES.CFB encrypted data
```
4. Use the password found in the last conversion
5. `You found a flag! <ykhti36b2thircqwr31sm17x7wpxsj4b>` inside the text


## Flag
`ykhti36b2thircqwr31sm17x7wpxsj4b`

## Tools 
- file
- exiftool
- binwalk
- strings
- (hexdump plus dur trouver data)
- binwalk
- foremost
tnx to Wyzeman
