---
title: set 1 - 5 - Implementando clave repetida XOR
layout: default
---

Implementando clave repetida XOR
================================

Aquí una estrofa de apertura de un importante trabaja del idioma inglés:

	Burning 'em, if you ain't quick and nimble
	I go crazy when I hear a cymbal

Cífrala, bajo la clave "ICE", utilizando XOR por clave repetida.

En XOR por clave repetida, aplicarás de forma secuencial cada byte de la clave; al primer byte del texto plano le aplicarás XOR contra la letra I, al siguiente contra la C, al siguiente contra la E y luego, nuevamente, el cuarto contra la I y así sucesivamente.

Deberías obtener:

	0b3637272a2b2e63622c2e69692a23693a2a3c6324202d623d63343c2a26226324272765272
	a282b2f20430a652e2c652a3124333a653e2b2027630c692b20283165286326302e27282f


Cifra unas cuántas cosas utilizando tu función de XOR por clave repetida. Cifra tu correo electrónico. Cifra tu archivo de contraseñas. Tu archivo sig. Acostúmbrate. Te lo prometo, no te estamos haciendo perder el tiempo con esto.