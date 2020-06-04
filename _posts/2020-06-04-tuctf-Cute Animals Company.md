---
layout: post
title:  Cute Animals Company - TU CTF 2019
image: ''
date:   2020-06-04
tags:
- ctf
- writeup
- web
description: 'Cute Animals Company - Writeup'
categories:
- WRITEUP 2019
- CTF
---

**Categoria: Web**

### Description:
```
Look at this cute website! Why don't you find some cute animals that are hidden from view?

chal.tuctf.com:30000
```
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute0.png" />


### Solve:
Acessando o link, temos:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute1.png" />
Porém, não obtivemos muitos resultados, então rodei o dirb em cima do site:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute2.png" />
Ao acessar "/admin.php", somos redirecionados para "/loginform.html", então tentei um sql injection no formulário:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute3.png" />
Na próxima página, é possível ver um login "bro/ultimate699":
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute4.png" />
Logando com essas credenciais:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute5.png" />
Redirecionados para "/portal.php":
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute6.png" />
No código fonte de "/portal.php" é possível ver um formulário com um parâmetro "file" que seria enviado via GET:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute7.png" />

Então, passando "file" como parâmetro e testando alguns payloads, me deparei com um LFI e explorei esse LFI com 
```
file:///etc/passwd
``` 
e assim obtendo a flag:
<img src="/assets/img/writeups/2019/TU CTF/Web/Cute Animals Company/cute8.png" />

### Flag:
```TUCTF{m0r3_cut3_4n1m415_c4n_b3_f0und_4t_https://bit.ly/1HU2m5Q}```