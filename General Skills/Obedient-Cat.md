# Obedient Cat

## Description
This file has a flag in plain sight (aka "in-the-clear").

Points: 5

## Flag
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}

## Resolution

```bash
bnichols108-picoctf@webshell:~$ mkdir obedient-cat
bnichols108-picoctf@webshell:~$ cd obedient-cat/
bnichols108-picoctf@webshell:~/obedient-cat$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
--2021-09-10 04:17:00--  https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                                100%[=================================================================================================================================================================>]      34  --.-KB/s    in 0s      

2021-09-10 04:17:00 (4.99 MB/s) - 'flag' saved [34/34]

bnichols108-picoctf@webshell:~/obedient-cat$ cat flag 
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
bnichols108-picoctf@webshell:~/obedient-cat$ 
```