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

## Navigation

### Sidebar

The book's automatically-generated table of contents is shown in the sidebar.

To show additional links above the table of contents in the sidebar,
define them in `sidebar_nav_top` in [_config.yml](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/_config.yml).

```yaml
sidebar_nav_top:
- label: About this site
  url: about.html
```

To show additional links at the bottom of the sidebar,
define them in `sidebar_nav_bottom` in [_config.yml](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/_config.yml).

```yaml
sidebar_nav_bottom:
- label: Privacy statement
  url: privacy.html
```

### Bottom of page

To change the links shown at the bottom of every page,
define them in `bottom_nav` in [_config.yml](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/_config.yml).

```yaml
bottom_nav:
- label: Home
  url: index.html
- label: Book
  url: book.html
- label: GitHub
  url: https://github.com/jasongrimes/jekyll-chapterbook
- label: Privacy
  url: privacy.html
```

### Breadcrumbs

To configure links to the book title page and table of contents in the chapter breadcrumbs,
specify the urls in `bookcrumbs` in [_config.yml](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/_config.yml). Each item is optional; comment it out to disable it.

```yaml
bookcrumbs:
  book_url: book.html
  contents_url: contents.html
  book_icon: assets/gitbook/images/apple-touch-icon-precomposed-152.png
```

## Include "helpers"

In order for this theme to work natively with GitHub pages,
it can't use any custom Jekyll plugins.
But it _can_ do any logic and data manipulation supported by the template language, Liquid.

So this theme makes extensive use of Liquid templates to act as "helpers",
by including them in a page and passing them parameters using Jekyll's standard [`include`](https://jekyllrb.com/docs/includes/) tag.

See [helpers in the demo](https://jasongrimes.github.io/jekyll-chapterbook/helpers.html) for details.

### Chapter links

The `chapter-link.html` helper renders a link to the chapter with the specified `slug`,
using its current title and chapter number.

For example:
{% raw %}
```
See {% include chapter-link.html slug="harmony-intro" %}.
```
{% endraw %}

Parameters:
- `slug`: Required. The `slug` of the chapter to link to.
- `anchor`: An optional anchor tag to append to the chapter link.

See an [example chapter link](https://jasongrimes.github.io/jekyll-chapterbook/helpers#chapter-links).

### Tables of contents

The `chapterbook-toc.html` helper allows you to make a table of contents page,
including chapter abstracts (if any).

Parameters:
- `show_drafts`: If `true`, also show draft chapters. Useful for showing an "outline" view of the book.

{% raw %}
```liquid
{% include chapterbook-toc.html %}
```
{% endraw %}

See an [example table of contents](https://jasongrimes.github.io/jekyll-chapterbook/contents.html)
and [draft outline](https://jasongrimes.github.io/jekyll-chapterbook/outline.html) in the demo.

### Figures

The `figure.html` helper renders images as figures in the book.

Parameters:
- `url`: The relative URL to the image (appended to `site.baseurl`).
- `caption`: An optional caption to render beneath the figure.
- `class`: an optional `class` attribute to add to the the HTML `<figure>` tag.

See an [example figure](https://jasongrimes.github.io/jekyll-chapterbook/helpers.html#figures) in the demo.

### Theme variables

The `chapter-vars.html` helper sets a number of variables related to chapters and parts
which can be accessed in markdown files or Liquid templates.
It can also render the variables for inspection,
to help with debugging.

Parameters:
- `id`: The `page.id` of the chapter page for which to set variables.
- `slug`: The `page.slug` of the chapter page for which to set variables (ignored if `id` is passed).
- `withnum`: For performance reasons, chapter and part numbers are not computed unless `withnum` is `true`. (To compute only chapter or only part numbers, set `withnum=part` or `withnum=chapter` instead.)
- `inspect`: If true, render the variables to the page, for debugging.

See [example chapter vars](https://jasongrimes.github.io/jekyll-chapterbook/variables.html) in the demo.

## Wide tables

Tables can be created using normal [GitHub-flavored markdown](https://github.github.com/gfm/#tables-extension-).

To prevent wide tables from breaking the book layout on mobile devices,
wrap them in a `<div>` directly in the markdown file,
with `class="table-wrapper"` and the attribute `markdown="block"`.

See an example of [mobile-friendly wide tables](https://jasongrimes.github.io/jekyll-chapterbook/wide-tables.html) in the demo.

## References and citations

See [example citations and references list](https://jasongrimes.github.io/jekyll-chapterbook/references.html) in the demo.

## Extra CSS or javascript files

You can add extra CSS or JavaScript references in `_config.yml`:

- `extra_css`: for additional style sheets. If the url does not start with http, the path must be relative to the root of the site, without a starting `/`.
- `extra_header_js`: for additional scripts to be included in the `<head>` tag, after the `extra_css` has been added. If the url does not start by http, the path must be relative to the root of the site, without a starting `/`.
- `extra_footer_js`: for additional scripts to be included at the end of the HTML document, just before the site tracking script. If the url does not start by http, the path must be relative to the root of the site, without a starting `/`.

## Customizing font settings

The fonts can be customized by modifying the `.book.font-family-0` and `.book.font-family-1` entry in `./assets/gitbook/custom.css`.

```css
.book.font-family-0 {
    font-family: Georgia, serif;
}
.book.font-family-1 {
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```


## License

Copyright &copy; 2023 Jason Grimes.

This work is open source,
made available under the [Apache License, Version 2.0](https://github.com/jasongrimes/jekyll-chapterbook/blob/master/LICENSE).

Originally based on [jekyll-gitbook](https://github.com/sighingnow/jekyll-gitbook),
which was Copyright 2019 Tao He,
and licensed under the [Apache License, Version 2.0](https://github.com/sighingnow/jekyll-gitbook/blob/f286e81abb57c91b7056d043d846cd308c8ea292/LICENSE).
