# Nice netcat...

## Description
There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net 43239, but it doesn't speak English...

Points: 15

## Flag
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir nice-netcat
bnichols108-picoctf@webshell:~$ cd nice-netcat/
bnichols108-picoctf@webshell:~/nice-netcat$ nc mercury.picoctf.net 43239
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
55 
99 
48 
56 
50 
49 
102 
53 
125 
10 
```
- Go to:
https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html
- Convert all numbers from Decimal (base10) to ASCII 
- Screenshot below:

<img src="Screenshots\Nice-netcat.jpg"
     alt="Screenshot for decimal to ASCII conversion"
     style="float: left; margin-right: 10px;" />