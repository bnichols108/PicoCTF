# Based

## Description
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with nc jupiter.challenges.picoctf.org 29221.

Points: 200

## Flag
picoCTF{learning_about_converting_values_00a975ff}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
socket
Please give the 01110011 01101111 01100011 01101011 01100101 01110100 as a word.
...
you have 45 seconds.....

Input:
socket
Please give me the  163 165 142 155 141 162 151 156 145 as a word.
Input:
submarine
Please give me the 6c69676874 as a word.
Input:
light
Youve beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```

- First conversion is from Binary to ASCII
- Screenshot below:

<img src="Screenshots\Based-1.jpg"
     alt="Screenshot for Binary to ASCII conversion"
     style="float: left; margin-right: 10px;" /> 
	 
- Second conversion is from Octal to Decimal to ASCII
- Screenshots below:

<img src="Screenshots\Based-2.jpg"
     alt="Screenshot for Octal to ASCII conversion"
     style="float: left; margin-right: 10px;" />
	 
- Third conversion is from Hex to ASCII
- Screenshot below:

<img src="Screenshots\Based-3.jpg"
     alt="Screenshot for Hex to ASCII conversion"
     style="float: left; margin-right: 10px;" />