---
layout: post
title:  Test Test Test - TU CTF 2019
image: ''
date:   2020-06-05
tags:
- ctf
- writeup
- web
description: 'Test Test Test  - Writeup'
categories:
- WRITEUP 2019
- CTF
--- 
**Category: Web**

### Description:
```
There are so many tests going on right now, why don't take a deep breath and list them out before you forget one?

chal.tuctf.com:30004
```
<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test0.png">

### Solve:
Ao acessar o site, temos a seguinte página:
<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test1.png">
Analisando o código fonte é possível ver um diretório chamado "/img":
<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test2.png">
Acessando esse diretório encontramos alguns arquivos:
<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test3.png">
E entrando em "/img/TODO.txt", tem-se:
<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test4.png">
E, então, usaremos o cURL para obter a flag, pois ao acessar ela somos redirecionados imediatamente para a página principal:

```
curl -v "http://chal.tuctf.com:30004/flag.php
```

<img src="/assets/img/writeups/2019/TU CTF/Web/Test Test Test/test5.png">

### Flag:
```TUCTF{d0nt_l34v3_y0ur_d1r3ct0ry_h4n61n6}```