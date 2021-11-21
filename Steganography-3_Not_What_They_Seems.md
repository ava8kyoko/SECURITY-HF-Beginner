# Steganography - 3 - Things Aren't Always What They Seem. (5)

## Challenge
This simple file contains 3 flags. Can you dig deep enough?
<br>
(Use file found during Flag #2)

## Steps
1. `ls` -> `FILE.jpg  FILE.zip  FILE.zip.gpg  FLAG2.txt  FLAG.mp3  FLAG.txt  FLAG.zip`
2. `file FLAG.mp3` -> `FLAG.mp3: XZ compressed data`
3. `mv FLAG.mp3 FLAG.xz`
4. `xz -d FLAG.xz`
5. `ls` -> `FILE.jpg  FILE.zip  FILE.zip.gpg  FLAG  FLAG2.txt  FLAG.txt  FLAG.zip`
6. `file FLAG` -> `FLAG: POSIX tar archive (GNU)`
7. `mv FLAG FLAG.tar `
8. `tar -xvf FLAG.tar` -> `FLAG.txt`
9. `file FLAG.txt` -> `FLAG.txt: ASCII text`
10. `cat FLAG.txt` -> `You found a flag! <w11wn5ar7ot0av4k83g768rxscv4kngl>`

## Flag
`w11wn5ar7ot0av4k83g768rxscv4kngl`
