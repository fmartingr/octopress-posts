---
comments: true
date: 2012-04-12 23:10:36
layout: post
slug: crear-una-imagen-y-su-reflejo-con-html-y-css3
title: Crear una imagen y su reflejo con HTML y CSS3
wordpress_id: 21
categories:
- Desarrollo web
tags:
- css3
- html5
---

![Prueba de reflejo con CSS3](http://cdn.fmartingr.com/blog/uploads/2012/04/css3-reflection.png)

**Disclaimer:** Se que esto no es una gran hazaña y que hay burradas de la leche con CSS3, que esto se podrá hacer de otra manera, etc. No soy diseñador, así que dejadme tranquilo. (XD)

Todo esto se me ocurrió ayer cuando estabamos revisando parte de los bocetos de una web, donde el diseño incluía una cabecera con una imagen y su reflejo. Dado que la imagen tenía que ser insertada por el usuario era totalmente inviable que el usuario lo crease de dicha manera, por lo que dije... ¿por qué no aprovechar los elemenos que nos brinda el movimiento HTML5?

Mentira. Lo primero que probé fue la cutrez de poner la altura de la imagen en negativo. Coño, igual colaba. Empecé a mirar por internet CSS3 y descubrí las transformaciones y los filtros (estos últimos para IE), y usando dichos atributos es posible voltear la imagen.

``` css
filter: FlipV;
-ms-filter: "FlipV";
-moz-transform: scaleY(-1);
-o-transform: scaleY(-1);
-webkit-transform: scaleY(-1);
transform: scaleY(-1);
```

Perfecto, ¡punto uno conseguido! Ahora puedo tener las dos imagenes viviendo juntas con una volteada, ahora hay que darle un efectillo degradado a transparente. Sí, ¿qué es HTML5 a parte de bordes redondeados y sombras? Gradientes :D

Para ello en mi caso y el código que podreis ver luego en github, creé una capa con dos dentro, una la imagen volteada y el gradiente para que pille el efecto. Se me fue la olla pero se entiende por donde va el tema, asi que...

En mi caso es un degradado de sin opacidad a blanco, dado que blanco es el fondo de la web que yo uso.

``` css 
/* FF3.6+ */
background: -moz-linear-gradient(top,
rgba(255,255,255,0.6) 0%,
rgba(255,255,255,1) 100%);
/* Chrome,Safari4+ */
background: -webkit-gradient(linear,
left top,
left bottom,
color-stop(0%,rgba(255,255,255,0.6)),
color-stop(100%,rgba(255,255,255,1)));
/* Chrome10+,Safari5.1+ */
background: -webkit-linear-gradient(top,
rgba(255,255,255,0.6) 0%,
rgba(255,255,255,1) 100%);
/* Opera 11.10+ */
background: -o-linear-gradient(top,
rgba(255,255,255,0.6) 0%,
rgba(255,255,255,1) 100%);
/* IE10+ */
background: -ms-linear-gradient(top,
rgba(255,255,255,0.6) 0%,
rgba(255,255,255,1) 100%);
/* W3C */
background: linear-gradient(top,
rgba(255,255,255,0.6) 0%,
rgba(255,255,255,1) 100%);
/* IE6-9 */
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#99ffffff', endColorstr='#ffffff',GradientType=0 );
```

Después de posicionar capas y demás os quedará el efecto que véis en la imagen de cabecera.

Como nota alternativa para cuando veáis lo de github: sí, se puede simplificar un montón, usar menos capas, ser más eficiente, etc etc etc. Esto es solo una muestra para que se pille el concepto.


**Código fuente de ejemplo |** [Github](https://github.com/fmartingr/fmartingr.github.com/tree/master/blog/css3-reflection) & [Demo](http://fmartingr.github.com/blog/css3-reflection/)

**Gracias a |** [Ultimate CSS Gradient Generator](http://www.colorzilla.com/gradient-editor/) y [CSS-Tricks - Flip an image](http://css-tricks.com/snippets/css/flip-an-image/)
