---
title: set 2 - 9 - Implementando relleno PKCS#7
layout: default
---

Implementando relleno PKCS#7
============================

Un cifrado por bloque transforma un bloque de texto plano de tamaño fijo (usualmente de 8 o 16 bytes) a un texto cifrado. Pero casi nunca se busca transforma un solo bloque; lo que se cifra son mensajes de tamaños irregulares.

Una forma de representar mensajes de largo irregular es mediante el relleno, creando un texto plano que es múltiplo del tamaño del bloque. El esquema de relleno más popular es el llamado PKCS#7.

Así que: rellena cualquier bloque a un tamaño específico, agregándole el número de bytes de relleno al final del bloque. Por ejemplo,

	"YELLOW SUBMARINE"

...rellenado a 20 bytes sería:

	"YELLOW SUBMARINE\x04\x04\x04\x04"