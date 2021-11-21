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
2. `steghide extract -sf FILE.jpg`


## Flag
``
