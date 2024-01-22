---
title: "Presentamos Decap CMS, una solución para la gestión de contenidos"
draft: false
author: Jorge Jimenez
tags:
  - decapcms
image:
  src: /images/decapcms.png
  alt: Decap CMS
snippet: Decap CMS, formerly known as Netlify CMS, is an open-source content
  management system offering developers a seamless way to manage content for
  static site generators.
publishDate: 2023-07-01 23:14
category: Tutoriales
---

Decap CMS, anteriormente conocido como Netlify CMS, es un sistema de administración de contenido de código abierto que ofrece a los desarrolladores una manera perfecta de administrar contenido para generadores de sitios estáticos.

## ¿Qué es Decap CMS?

Decap CMS es un CMS basado en Git que permite a los desarrolladores y creadores de contenido agregar, actualizar y eliminar contenido directamente desde el repositorio de Git del sitio. Esto proporciona los beneficios del contenido controlado por versión, lo que permite reversiones, bifurcaciones y otras operaciones de Git fácilmente.

## Características clave de Decap CMS

### Fuente abierta

Ser de código abierto significa que tiene acceso al código fuente y puede modificarlo y personalizarlo según los requisitos de su proyecto. Esto permite una gran flexibilidad a la hora de adaptar el CMS a sus necesidades específicas.

### Basado en Git

Decap CMS utiliza flujos de trabajo de Git para la gestión de contenidos. Cada edición se convierte en una confirmación, cada lote de ediciones se convierte en una solicitud de extracción y cada borrador guardado es solo una rama.

### Fácil de usar

Decap CMS proporciona una interfaz editorial fácil de usar para los creadores de contenido, liberándolos de la necesidad de comprender Git o código.

## Primeros pasos con Decap CMS

Comenzar con Decap CMS es tan fácil como agregar dos archivos a su proyecto: `admin/index.html` y `admin/config.yml`.

```html
<!-- admin/index.html -->
<!doctype html>
<html>
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Content Manager</title>
</head>
<body>
  <!-- Include the script that builds the page and powers Decap CMS -->
  <script src="https://unpkg.com/decap-cms@^2.0.0/dist/decap-cms.js"></script>
</body>
</html>
```

```yaml
# admin/config.yml
backend:
  name: github
  repo: owner/repo
media_folder: "img/uploads"
public_folder: "/img/uploads"
collections:
  - name: "post"
    label: "Post"
    folder: "_posts"
    create: true
    fields:
      - {label: "Title", name: "title", widget: "string"}
      - {label: "Body", name: "body", widget: "markdown"}
```

En la era de Jamstack, Decap CMS está allanando el camino para la gestión de contenidos moderna basada en Git. Con su simplicidad y flexibilidad, es una excelente opción tanto para desarrolladores como para creadores de contenido.
