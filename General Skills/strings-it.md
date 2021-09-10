# strings it

## Description
Can you find the flag in file without running it?

Points: 100

## Flag
picoCTF{5tRIng5_1T_827aee91}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir strings-it
bnichols108-picoctf@webshell:~$ cd strings-it/
bnichols108-picoctf@webshell:~/strings-it$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
--2021-09-10 06:05:06--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                                             100%[=================================================================================================================================================================>] 757.84K  1.86MB/s    in 0.4s    

2021-09-10 06:05:07 (1.86 MB/s) - 'strings' saved [776032/776032]

bnichols108-picoctf@webshell:~/strings-it$ ll
total 764
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf     21 Sep 10 06:05 ./
drwxr-xr-x 18 bnichols108-picoctf bnichols108-picoctf   4096 Sep 10 06:04 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 776032 Oct 26  2020 strings
bnichols108-picoctf@webshell:~/strings-it$ strings strings | grep pico 
picoCTF{5tRIng5_1T_827aee91}
```