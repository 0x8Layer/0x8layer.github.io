---
layout: post
title:  OpenDoor - TU CTF 2019
image: ''
date:   2020-06-05
tags:
- ctf
- writeup
- web
description: 'OpenDoor - Writeup'
categories:
- WRITEUP 2019
- CTF
---
**Category: Web**

### Description:
```
This challenge is an open door; show us you know how to find the key.

chal.tuctf.com:30002
```

<img src="/assets/img/writeups/2019/TU CTF/Web/OpenDoor/opendoor0.png" />

### Solve:
Acessando a página web, temos:
<img src="/assets/img/writeups/2019/TU CTF/Web/OpenDoor/opendoor1.png" />
E analisando o código fonte foi possível encontrar a flag:
<img src="/assets/img/writeups/2019/TU CTF/Web/OpenDoor/opendoor2.png" />

### Flag:
```TUCTF{f1r5t_fl46_345135t_fl46}```