---
title: los desafíos de cifrado de el matasano
layout: default
---

Bienvenido a los desafíos
=========================

<div class="warning">
<h3>Trabajo en progreso.</h3>

<p>Este sitio contendrá los ocho sets de los desafíos de cifrado, con soluciones en los lenguajes principales.</p>
</div>

Pero: aún no. Si esperamos a darle a "publicar" cuando esté todo terminado, podríamos aún estar escribiendo esto en 2015 (_Nota del traductor_: ya estamos en 2015 y el último set aún no está publicado). Así que iremos publicando a medida que vayamos avanzando. En particular: danos un poco de tiempo en la publicación de las soluciones.

No podemos introducir esto de una mejor forma a como lo hizo [Maciej Ceglowski](https://blog.pinboard.in/2013/04/the_matasano_crypto_challenges/), así que lee primero ese artículo.

Hemos creado una colección de 48 ejercicios que demuestran ataques de cifrado en el mundo real.

Esta es una forma diferente de aprender acerca de cifrado a tomar una clase o leer un libro. Te daremos problemas a resolver. Son derivados de debilidades en sistemas en el mundo real y construcciones de cifrado modernas. Te daremos suficiente información para que aprendas acerca de los conceptos fundamentales por ti mismo. Cuando finalices, no solamente tendrás un conocimiento acerca de cómo los sistema de cifrado están construidos, sino también cómo son atacados.

##¿Cuáles son las reglas?

¡No hay ninguna! Durante muchos años hemos impulsado estos desafíos por correo electrónico, pidiéndole a los participantes que no compartan sus resultados. ¡El sistema de honor funcionó de mil maravillas! Pero ahora estamos listos para poner a un lado la ceremonia, publicar los desafíos y que todos puedan trabajar en ellos.

##¿Cuánto necesito saber?

Si tienes algún problema con las matemáticas en estos desafíos, deberías ser capaz de encontrar algún alumno de noveno año que te ayude. Resulta que las matemáticas que muchos ataques de cifrado moderno realizan son bastante elementales.

##¿Cuánto debo saber de cifrado?

Nada. Esa es la idea.

##Así que, ¿qué debo saber?

Deberías ser capaz de escribir código de forma profesional en algún lenguaje de programación. Hemos recibido soluciones en C, C++, Python, Ruby, Perl, Visual Basic, X86 Assembly, Haskell, y Lisp. Sorpréndenos con algún otro lenguaje. Nuestro amigo Maciej dice que estos desafíos son buenos para aprender un nuevo lenguaje, así que que quizás sea el momento de elegir alguno como Clojure o Rust.

##¿Qué debería esperar?

Ahora mismo tenemos siete sets. Su dificultad aumente progresivamente. De nuevo: están basados en vulnerabilidades del mundo real. Ninguno de ellos es un "puzzle". Ninguno de ellos está diseñado para hacerte tropezar. Algunos de estos ataques son inteligente, y si no estás familiarizado con la astucia de cifrado... bueno, debería gustarte solucionar puzzles. Un reconocimiento al hip-hop de MTV de principios de los '90 tampoco está mal.



##¿Pueden darme una larga explicación de porqué han decidido hacer esto?

_Resulta que sí podemos._

Si no estás familiarizado con el cifrado o si tu conocimiento viene de cosas como Criptografía Aplicada, esto puede sorprenderte: la mayor parte del cifrado está fatalmente dañado. Los sistemas en los que confiamos hoy en día y que no se sepa que están fatalmente dañados están en camino a estarlo. Nadie está seguro de que TLS 1.2 o SSH 2 o OTR vayan a permanecer seguros de la manera en que fueron diseñados.

El estado actual de los programas informáticos de seguridad de cifrado es similar al estado de los programas de seguridad en la década de los '90. Específicamente: hasta cerca de 1995, no era de conocimiento popular que los programas diseñados por humanos pudiesen tener problemas de cálculo. Como resultado, nadie puedo establecer un tamaño apropiado para un buffer, y la humanidad se ha pasado más de una década y media gastando miles de millones de dólares corrigiendo vulnerabilidades de memoria corrupta.

El cálculo no es un problema difícil. Pero el cifrado sí lo es. Hay pocas cosas que puedes hacer para equivocarte al calcular el tamaño de un buffer. Pero hay decenas, probablemente cientos de pequeñas y oscuras cosas que puedes hacer para tomar un sistema de cifrado que debería se seguro, incluso contra un adversario con más núcleos de CPU (Unidad central de procesamiento) que átomos en el sistema solar, y resolverlo con un script en Perl en 15 segundos. No nos creas a nosotros: haz los desafíos y verás.

La gente ya "sabe" esto, pero realmente no están convencidos, y creemos que la razón de ello es que hay realmente muy pocas personas que saben cómo implementar los ataques más conocidos. Así que, envíanos un correo y te contaremos acerca de ellos.

##¿Cómo comienzo?

[¡Comienza aquí!](set_1.md)

##¿Quién ha hecho esto?

- Thomas Ptacek ([@tqbf](https://twitter.com/tqbf))
- Sean Devlin ([@spdevlin](https://twitter.com/spdevlin))
- Alex Balducci ([@iamalexalright](https://twitter.com/iamalexalright))
- Marcin Wielgoszewski ([@marcinw](https://twitter.com/marcinw))

No podríamos haber realizado esto sin la ayuda de muchas otras personas. Aproximadamente en orden de influencia: 

- [Nate Lawson](http://www.rootlabs.com/) nos enseñó virtualmente todo lo que sabemos sobre cifrado.
- [Trevor Perrin](http://trevp.net/) le enseño alguna cosa a Nate. Puedo contarte una historia bastante convincente acerca de cómo Trevor es el origen intelectual de cada ataque exitoso sobre TLS en los últimos 5 años.
- Thai Duong y Juliano Rizzo son los padrinos de los programas prácticos de seguridad de cifrado. Muchas cosas en estos desafíos no tenían sentido para nosotros hasta que Thai y Juliano las explotaron.
