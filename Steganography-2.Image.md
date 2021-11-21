#  Steganography - 2 - An Image is Worth a Thousand Words. (5)

## Challenge
This simple file contains 3 flags. Can you dig deep enough?
<br>
(Use file found during Flag #1)

## Steps
1. `file FILE.jpg`
```FILE.jpg: JPEG image data, JFIF standard 1.01, 
aspect ratio, density 1x1, segment length 16, 
baseline, precision 8, 640x400, components 3
```
2. Open FILE.jpg
``` The BASE of the problem might be steganography.
d2VsbFBsYXllZA==
```
No... it's not "II", but "ll"
3. <a href="https://www.base64decode.org/">Converte Base64 to ASCII</a> -> `wellPlayed`
4. `steghide extract -sf FILE.jpg`
5. Use the last conversion as passphrase -> `wrote extracted data to "FLAG.zip".`
6. `ls`  -> `FILE.jpg  FILE.zip  FILE.zip.gpg  FLAG.txt  FLAG.zip`
7. `flag FLAG.zip` -> `FLAG.zip: Zip archive data, at least v1.0 to extract`
8. `unzip FLAG.zip`
``` Archive:  FLAG.zip
 extracting: FLAG.mp3                
replace FLAG.txt? [y]es, [n]o, [A]ll, [N]one, [r]ename: r
new name: FLAG2.txt
 extracting: FLAG2.txt   
 ```
9. `cat FLAG2.txt` -> `You found a flag! <b05kruwi3bwczluxupgewpacy2liglfe>`

## Flag
`b05kruwi3bwczluxupgewpacy2liglfe`

## Tool
- hash-identifier
