# plumbing

## Description
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org 7480.

Points: 200

## Flag
picoCTF{digital_plumb3r_06e9d954}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir plumbing
bnichols108-picoctf@webshell:~$ cd plumbing/
bnichols108-picoctf@webshell:~/plumbing$ nc jupiter.challenges.picoctf.org 7480 
.
.
.
This is defintely not a flag
Again, I really dont think this is a flag
Not a flag either
Not a flag either
This is defintely not a flag
This is defintely not a flag
I dont think this is a flag either
Not a flag either
Again, I really dont think this is a flag
I dont think this is a flag either
I dont think this is a flag either
Not a flag either
Not a flag either
I dont think this is a flag either
Again, I really dont think this is a flag
.
.
.
bnichols108-picoctf@webshell:~/plumbing$ nc jupiter.challenges.picoctf.org 7480 > plumbing.txt; grep -i picoctf plumbing.txt
picoCTF{digital_plumb3r_06e9d954}
```