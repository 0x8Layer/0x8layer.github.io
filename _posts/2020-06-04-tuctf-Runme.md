---
layout: post
title:  Runme - TU CTF 2019
image: ''
date:   2020-06-04
tags:
- ctf
- writeup
- pwn
description: 'Runme - Writeup'
categories:
- WRITEUP 2019
- CTF
---

**Category: Pwn**

### Description:
```
Everyone starts somewhere.
```

### Solve:
Apenas executar o binário e digitar "flag":
```
root@kali:~/pwn/runme# ./runme 
Enter 'flag'
> flag
TUCTF{7h4nk5_f0r_c0mp371n6._H4v3_fun,_4nd_600d_luck}
```
Ou usar strings no binário:
```
root@kali:~/pwn/runme# strings runme 
[...]
u+UH
[]A\A]A^A_
Enter 'flag'
flag
TUCTF{7h4nk5_f0r_c0mp371n6._H4v3_fun,_4nd_600d_luck}
How did you fail that?
:*3$"
[...]
```

### Flag:
```TUCTF{7h4nk5_f0r_c0mp371n6._H4v3_fun,_4nd_600d_luck}```
