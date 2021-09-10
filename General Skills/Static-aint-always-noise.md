# Static ain't always noise

## Description
Can you look at the data in this binary: static? This BASH script might help!

Points: 20

## Flag
picoCTF{d15a5m_t34s3r_1e6a7731}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir static-aint-always-noise
bnichols108-picoctf@webshell:~$ cd static-aint-always-noise/
bnichols108-picoctf@webshell:~/static-aint-always-noise$ wget https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh
--2021-09-10 04:53:27--  https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                                              100%[=================================================================================================================================================================>]   8.18K  --.-KB/s    in 0s      

2021-09-10 04:53:27 (130 MB/s) - 'static' saved [8376/8376]

--2021-09-10 04:53:27--  https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh
Reusing existing connection to mercury.picoctf.net:443.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                                            100%[=================================================================================================================================================================>]     785  --.-KB/s    in 0s      

2021-09-10 04:53:27 (95.2 MB/s) - 'ltdis.sh' saved [785/785]

FINISHED --2021-09-10 04:53:27--
Total wall clock time: 0.04s
Downloaded: 2 files, 8.9K in 0s (126 MB/s)
bnichols108-picoctf@webshell:~/static-aint-always-noise$ ll
total 20
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf   36 Sep 10 04:53 ./
drwxr-xr-x 13 bnichols108-picoctf bnichols108-picoctf 4096 Sep 10 04:53 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf  785 Mar 16 00:53 ltdis.sh
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 8376 Mar 16 00:53 static
bnichols108-picoctf@webshell:~/static-aint-always-noise$ file static    
static: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=33934f7b8aea8e359749ed57dca4cd26d6059acf, not stripped
bnichols108-picoctf@webshell:~/static-aint-always-noise$ strings static | grep pico
picoCTF{d15a5m_t34s3r_1e6a7731}
```