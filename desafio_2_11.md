---
title: set 2 - 11 - Un oráculo de detección ECB/CBC
layout: default
---

Un oráculo de detección ECB/CBC
===============================

Ahora que tienes ECB y CBC funcionando:

Escribe una función para generar llaves AES al azar; esto es, 16 bytes al azar.

Escribe una función que cifra información bajo una llave desconocida; esto es, una función que genera llaves al azar y cifra utilizándolas.

La función debe verse así:

	encryption_oracle(tu-texto)
	=> [GARABATOS SIN SENTIDO]

Por debajo, has que la función _agregue_ de 5 a 10 bytes (este valor se elije al azar) _antes_ del texto plano y de 5 a 10 bytes _después_ del texto plano.

Ahora, la función debe elegir cifrar bajo ECB la mitad de las veces, y bajo CBC la otra mitad (utiliza IVs al azar cada vez para CBC). Utiliza rand(2) para elegir cual utilizar.

Detecta qué modo de cifrado por bloque es utilizado en cada oportunidad. Deberías terminar con un código que, evaluando un bloque que puede estar cifrado con ECB o CBC, determina cuál de los dos es utilizado.