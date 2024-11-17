---
title: Referencias
slug: references
disable_toc: true
#class: references
---

Este es un capítulo de ejemplo para citar referencias.

Consulte el [Scribbr citation generator](https://www.scribbr.com/citation/generator/) para generar citas en el estilo deseado. (Estos ejemplos utilizan el estilo APA).



### Citas en el texto

A continuación se muestra un ejemplo de cita que se incluirá en un texto, con un enlace al capítulo de referencias:

```
[(Berg, 1997)](references.html#berg-1997)
```

…lo que se traduce como [(Berg, 1997)](references.html#berg-1997).

### Lista de referencias


Utilice un capítulo de “referencias” al final del libro para enumerar todas las citas completas y recibir enlaces entrantes de las citas en el texto.

Para utilizar un estilo de cita con “sangría francesa” como APA, colóquelo `class: references` ien la introducción de la página de referencias o envuélvalo en un div como este directamente en el markdown:

{% raw %}
```html
<div class="references" markdown="block">
```
{% endraw %}

Para que funcionen los enlaces de anclaje entrantes desde citas en el texto, tenemos que incluir un enlace en cada referencia (como el enlace ISBN a continuación) y asignarle un `id` atributo con  `{:#my-id}`.

{% raw %}
```
Berg, C. (1997). *Mastering Guitar Technique: Process and Essence (Classic Guitar).* Mel Bay Publications, Inc.
[ISBN 978-1-610-65058-8](https://en.wikipedia.org/wiki/Special:BookSources?isbn=978-1-610-65058-8){:#berg-1997}.
```
{% endraw %}

…que se muestra a continuación.



## Referencias

Berg, C. (1997). *Mastering Guitar Technique: Process and Essence (Classic Guitar).* Mel Bay Publications, Inc.
[ISBN 978-1-610-65058-8](https://en.wikipedia.org/wiki/Special:BookSources?isbn=978-1-610-65058-8){:#berg-1997}.

Berg, C. (2019). *Practicing Music by Design: Historic Virtuosi on Peak Performance* (1st ed.). Routledge.
[ISBN 978-0-429-57631-7](https://en.wikipedia.org/wiki/Special:BookSources?isbn=978-0-429-57631-7){:#berg-2019}.


---

---
