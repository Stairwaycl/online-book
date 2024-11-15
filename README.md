---
layout: home
title: Plantilla Jekyll 1
permalink: /
---

Este es un tema  [Jekyll](https://jekyllrb.com/) basado en [GitBook](https://www.gitbook.com/) que agrega soporte para organizar fácilmente las páginas en capítulos y partes de libros. No depende de ningún complemento, por lo que funciona de forma nativa con [GitHub Pages](https://pages.github.com/).

Este tema se basó en el tema [jekyll-chapterbook de Jason Grimes](https://github.com/jasongrimes/jekyll-chapterbook).

## Demos

### Demo en GitHub pages

[stairwaycl.github.io/jekyll-chapterbook/](https://stairwaycl.github.io/jekyll-chapterbook/)

Also see its
[GitHub repo](https://github.com/stairwaycl/jekyll-chapterbook).

## Por qué este tema

Está pensado para ayudar a escribir un libro de forma gradual durante un largo período de tiempo, comenzando con una idea y construyendo lentamente capítulos y partes.

Fue creado con los siguientes objetivos:

* Genere una carpeta portátil y plana de HTML estático que se puede usar sin conexión o alojar en cualquier lugar.
Admite todas las partes estándar de un libro, incluidas las portadas, las contraportadas, los capítulos, las partes, etc.
* Admite la reorganización frecuente de capítulos y partes sin romper los vínculos existentes.
* Hacer que el trabajo en progreso esté disponible públicamente de una manera útil, al tiempo que se hacen disponibles los borradores que no están listos para el consumo público sin interrumpir el flujo de capítulos completados.
* Ejecútelo de forma nativa en páginas de GitHub sin complementos personalizados.
* Numerar automáticamente partes y capítulos.
* Haga que los archivos fuente de Markdown de cada capítulo aparezcan en orden en el sistema de archivos y en GitHub, independientemente del nombre del capítulo, sin tener que renumerarlos manualmente. (Esto hace que sea más fácil encontrar la página que desea editar).


## Wide tables

Se pueden crear tablas usando el común [GitHub-flavored markdown](https://github.github.com/gfm/#tables-extension-).

Para evitar que las tablas anchas interrumpan el diseño del libro en dispositivos móviles, envuélvalas `<div>` directamente en el markdown file con `class="table-wrapper"` y el attribute `markdown="block"`.

Vea un ejemplo de [mobile-friendly wide tables](https://jasongrimes.github.io/jekyll-chapterbook/wide-tables.html) en el demo.

## References and citations

Vea [ejemplo de lista de citas y referencias](https://stairwaycl.github.io/jekyll-chapterbook/references.html)en la demo.

## Personalizar la configuración de fuentes

Las fuentes se pueden personalizar modificando la entrada


## License

Copyright &copy; 2024 Gatica y Mongelós SpA.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


Made available under the [Apache License, Version 2.0](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/LICENSE).

Originally based on [jekyll-gitbook](https://github.com/sighingnow/jekyll-gitbook),
which was Copyright 2019 Tao He,
and licensed under the [Apache License, Version 2.0](https://github.com/sighingnow/jekyll-gitbook/blob/f286e81abb57c91b7056d043d846cd308c8ea292/LICENSE).
