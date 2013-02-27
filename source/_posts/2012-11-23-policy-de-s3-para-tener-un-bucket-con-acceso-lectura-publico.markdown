---
comments: true
date: 2012-11-23 10:36:42
layout: post
slug: policy-de-s3-para-tener-un-bucket-con-acceso-lectura-publico
title: Policy de S3 para tener un bucket con acceso lectura público
wordpress_id: 85
categories:
- Desarrollo web
tags:
- Amazon
- S3
---

Después de haber migrado el blog a un servicio PaaS -que ya comentaré en otra entrada-, tuve el problemilla de que el espacio en disco era volatil y tenía que guardar las imágenes y demás en un servidor o CDN a parte. Ya puestos, a tirar la casa por la ventana, decidí usar S3.

Creé un bucket que voy a usar como CDN a partir de ahora, pero trasteando vi que los permisos había que incluirlos por fichero, lo cual era un engorro. Investigando encontré las Policy, que son cadenas JSON puedes indicar propiedades a todo el Bucket.

Pues bien, para hacer un bucket público al completo lo que tenéis que poner en vuestras policy es esto:

``` javascript
{
    "Version": "2008-10-17",
    "Statement": [{
        "Sid": "AllowPublicRead",
        "Effect": "Allow",
        "Principal": {
            "AWS": "*"
        },
        "Action": ["s3:GetObject"],
        "Resource": ["arn:aws:s3:::<nombre del bucket>/*"]
    }]
}
```

Sustituís <nombre del bucket> por el nombre del vuestro y lo aplicáis. Con esto tendréis todo el contenido de vuestro bucket disponible para todo el mundo, pero si queréis ser más restrictivos y hacer pública solo una carpeta lo especificáis en el atributo Resource:


``` javascript
"Resource": ["arn:aws:s3:::<nombre del bucket>/<carpeta>/*"]
```

Espero que os sirva de ayuda.
