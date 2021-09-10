# First Grep

## Description
Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way.

Points: 100

## Flag
picoCTF{grep_is_good_to_find_things_dba08a45}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir first-grep
bnichols108-picoctf@webshell:~$ cd first-grep/
bnichols108-picoctf@webshell:~/first-grep$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
--2021-09-10 06:11:45--  https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                                                100%[=================================================================================================================================================================>]  14.21K  --.-KB/s    in 0s      

2021-09-10 06:11:45 (382 MB/s) - 'file' saved [14551/14551]

bnichols108-picoctf@webshell:~/first-grep$ ll
total 20
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf    18 Sep 10 06:11 ./
drwxr-xr-x 19 bnichols108-picoctf bnichols108-picoctf  4096 Sep 10 06:11 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 14551 Oct 26  2020 file
bnichols108-picoctf@webshell:~/first-grep$ file file 
file: ASCII text, with very long lines
bnichols108-picoctf@webshell:~/first-grep$ grep -i picoctf file 
picoCTF{grep_is_good_to_find_things_dba08a45}
```