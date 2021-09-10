# Python Wrangling

## Description
Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

Points: 10

## Flag
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir python-wrangling
bnichols108-picoctf@webshell:~$ cd python-wrangling/
bnichols108-picoctf@webshell:~/python-wrangling$ wget https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en
--2021-09-10 04:34:51--  https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: 'ende.py'

ende.py                                                             100%[=================================================================================================================================================================>]   1.30K  --.-KB/s    in 0s      

2021-09-10 04:34:51 (141 MB/s) - 'ende.py' saved [1328/1328]

--2021-09-10 04:34:51--  https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt
Reusing existing connection to mercury.picoctf.net:443.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: 'pw.txt'

pw.txt                                                              100%[=================================================================================================================================================================>]      33  --.-KB/s    in 0s      

2021-09-10 04:34:51 (1.74 MB/s) - 'pw.txt' saved [33/33]

--2021-09-10 04:34:51--  https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en
Reusing existing connection to mercury.picoctf.net:443.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: 'flag.txt.en'

flag.txt.en                                                         100%[=================================================================================================================================================================>]     140  --.-KB/s    in 0s      

2021-09-10 04:34:51 (22.9 MB/s) - 'flag.txt.en' saved [140/140]

FINISHED --2021-09-10 04:34:51--
Total wall clock time: 0.03s
Downloaded: 3 files, 1.5K in 0s (43.5 MB/s)
bnichols108-picoctf@webshell:~/python-wrangling$ ll
total 12
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf   54 Sep 10 04:34 ./
drwxr-xr-x 10 bnichols108-picoctf bnichols108-picoctf  284 Sep 10 04:16 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 1328 Mar 16 00:55 ende.py
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf  140 Mar 16 00:55 flag.txt.en
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf   33 Mar 16 00:55 pw.txt
bnichols108-picoctf@webshell:~/python-wrangling$ cat pw.txt 
aa821c16aa821c16aa821c16aa821c16
bnichols108-picoctf@webshell:~/python-wrangling$ python ende.py -d flag.txt.en
Please enter the password:aa821c16aa821c16aa821c16aa821c16
picoCTF{4p0110_1n_7h3_h0us3_aa821c16}
bnichols108-picoctf@webshell:~/python-wrangling$
```