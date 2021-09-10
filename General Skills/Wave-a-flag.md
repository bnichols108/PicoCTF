# Wave a flag

## Description
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

Points: 10

## Flag
picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

## Resolution
```bash
Wave-a-flag

bnichols108-picoctf@webshell:~$ mkdir wave-a-flag
bnichols108-picoctf@webshell:~$ cd wave-a-flag/
bnichols108-picoctf@webshell:~/wave-a-flag$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2021-09-10 04:38:55--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                                100%[=================================================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2021-09-10 04:38:56 (116 MB/s) - 'warm' saved [10936/10936]

bnichols108-picoctf@webshell:~/wave-a-flag$ ll
total 12
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf    18 Sep 10 04:38 ./
drwxr-xr-x 11 bnichols108-picoctf bnichols108-picoctf   303 Sep 10 04:38 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 10936 Mar 16 01:04 warm
bnichols108-picoctf@webshell:~/wave-a-flag$ file warm 
warm: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3181a501366281ab5eba1c41e54a1f40800e3966, with debug_info, not stripped
bnichols108-picoctf@webshell:~/wave-a-flag$ strings warm | grep flag
Oh, help? I actually dont do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
_flags
_flags2
/opt/hacksports/shared/staging/Wave a flag_4_7565734964921504/problem_files
bnichols108-picoctf@webshell:~/wave-a-flag$
```