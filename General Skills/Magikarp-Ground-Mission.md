# Magikarp Ground Mission

## Description
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `6d448c9c`

Points: 30

## Flag
picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir magikarp-ground-mission
bnichols108-picoctf@webshell:~$ cd magikarp-ground-mission/
bnichols108-picoctf@webshell:~/magikarp-ground-mission$ ssh ctf-player@venus.picoctf.net -p 60019
The authenticity of host '[venus.picoctf.net]:60019 ([3.131.124.143]:60019)' can't be established.
ECDSA key fingerprint is ***************************************.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[venus.picoctf.net]:60019,[3.131.124.143]:60019' (ECDSA) to the list of known hosts.
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
5190b070}
ctf-player@pico-chall$ cat ~/drop-in/1of3.flag.txt /2of3.flag.txt ~/3of3.flag.txt | tr '\n' ' '
picoCTF{xxsh_ 0ut_0f_\/\/4t3r_ 5190b070} ctf-player@pico-chall$ 