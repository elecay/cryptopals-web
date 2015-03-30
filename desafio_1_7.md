---
title: set 1 - 7 - AES en modo ECB
layout: default
---

AES en modo ECB
===============

El contenido codificado en base64 en [este archivo]({{ site.baseurl }}/7.txt) ha sido cifrado vía AES-128 en modo ECB bajo la clave:

	YELLOW SUBMARINE

(las mayúsculas y minúsculas importan; exactamente 16 caracteres; a mi me gusta "YELLOW SUBMARINE" porque tiene exactamente 16 bytes de largo y ahora a ti también.)

Descífralo. Después de todo ya sabes la clave.

Forma fácil: utiliza OpenSSL::Cipher y elige AES-128-ECB como forma de cifrado.

<div class="warning">
<h3>Hazlo con código</h3>

<p>Evidentemente puedes descifrarlo utilizando la herramienta de linea de comando de OpenSSL, pero estamos haciendo que tengas ECB funcionando en tu código por una razón. Vas a necesitarlo mucho más adelante, y no solamente para atacar ECB.</p>
</div>