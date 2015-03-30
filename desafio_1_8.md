---
title: set 1 - 8 - Detectando AES en modo ECB
layout: default
---

Detectando AES en modo ECB
==========================

En [este archivo]({{ site.url }}/8.txt) hay unos cuantos textos cifrados codificados a hex.

Uno de ellos ha sido cifrado con ECB.

Detéctalo.

Recuerda que el problema con ECB es que no tiene estado y es determinista; el mismo bloque de texto plano de 16 bytes producirá siempre el mismo texto cifrado de 16 bytes.