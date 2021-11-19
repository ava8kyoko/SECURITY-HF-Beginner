# - Hidden file

## Challenge
Get a shell as the user cerealkiller with the previous SSH key and look for a hidden file.
<br> <br>
Requirement: You need to have done the SSH Challenge first

## Steps

1. `ssh cerealkiller@beginner-linux.hfctf.ca -i /tmp/mozilla_kali0/id_ed25519`
2. `ls -la`
3. `cd .hidden`
4. `ls`
5. `cat flag.txt`

## Flag
`HF-48A5B31EDB33E1DA01913DD63AF8707D`
