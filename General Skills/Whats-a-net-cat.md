# what's a net cat?

## Description
Using netcat (nc) is going to be pretty important. Can you connect to jupiter.challenges.picoctf.org at port 64287 to get the flag?

Points: 100

## Flag
picoCTF{nEtCat_Mast3ry_284be8f7}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir whats-a-net-cat
bnichols108-picoctf@webshell:~$ cd whats-a-net-cat/
bnichols108-picoctf@webshell:~/whats-a-net-cat$ nc jupiter.challenges.picoctf.org 64287 
Youre on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_284be8f7}
```