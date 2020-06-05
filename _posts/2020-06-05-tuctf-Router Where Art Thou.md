---
layout: post
title:  Router Where Art Thou - TU CTF 2019
image: ''
date:   2020-06-05
tags:
- ctf
- writeup
- web
description: 'Router Where Art Thou - Writeup'
categories:
- WRITEUP 2019
- CTF
---
**Category: Web**

### Description
```
Interesting login page, think you can crack it?

chal.tuctf.com:30006
```
<img src="/assets/img/writeups/2019/TU CTF/Web/Router Where Art Thou/router0.png" />

### Solve:
Como o nome do desafio fala sobre roteador e a descrição sobre invadir uma página de login, nada melhor que tentar algumas senhas "defaults" dos roteadores.

Comecei por "admin/admin":
<img src="/assets/img/writeups/2019/TU CTF/Web/Router Where Art Thou/router1.png" />
E, então, aqui está a flag:
<img src="/assets/img/writeups/2019/TU CTF/Web/Router Where Art Thou/router2.png" />

### Flag:
```TUCTF{y0u_f0und_th3_fun_r0ut3r_d3f4ult5}```