# Tab, Tab, Attack

## Description
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip

Points: 20

## Flag
picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir tab-tab-attack
bnichols108-picoctf@webshell:~$ cd tab-tab-attack/
bnichols108-picoctf@webshell:~/tab-tab-attack$ wget https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip
--2021-09-10 05:29:03--  https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                                                100%[=================================================================================================================================================================>]   4.41K  --.-KB/s    in 0s      

2021-09-10 05:29:03 (551 MB/s) - 'Addadshashanammu.zip' saved [4520/4520]

bnichols108-picoctf@webshell:~/tab-tab-attack$ ll
total 12
drwxrwxr-x  2 bnichols108-picoctf bnichols108-picoctf   34 Sep 10 05:29 ./
drwxr-xr-x 14 bnichols108-picoctf bnichols108-picoctf 4096 Sep 10 05:28 ../
-rw-rw-r--  1 bnichols108-picoctf bnichols108-picoctf 4520 Mar 16 01:16 Addadshashanammu.zip
bnichols108-picoctf@webshell:~/tab-tab-attack$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
bnichols108-picoctf@webshell:~/tab-tab-attack$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
bnichols108-picoctf@webshell:~/tab-tab-attack/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ll
total 12
drwxr-xr-x 2 bnichols108-picoctf bnichols108-picoctf   35 Mar 16 01:16 ./
drwxr-xr-x 3 bnichols108-picoctf bnichols108-picoctf   27 Mar 16 01:16 ../
-rwxr-xr-x 1 bnichols108-picoctf bnichols108-picoctf 8320 Mar 16 01:16 fang-of-haynekhtnamet*
bnichols108-picoctf@webshell:~/tab-tab-attack/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ file fang-of-haynekhtnamet 
fang-of-haynekhtnamet: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=e34ce4e4ee2f7ce7fb251c8f5ab036da9882bc55, not stripped
bnichols108-picoctf@webshell:~/tab-tab-attack/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ strings fang-of-haynekhtnamet | grep pico
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}