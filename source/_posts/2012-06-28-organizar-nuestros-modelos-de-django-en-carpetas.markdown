---
comments: true
date: 2012-06-28 04:23:14
layout: post
slug: organizar-nuestros-modelos-de-django-en-carpetas
title: Organizar nuestros modelos de django en carpetas
wordpress_id: 60
categories:
- Desarrollo web
tags:
- django
- insomnio
- python
---

{% img left http://cdn.fmartingr.com/blog/uploads/2012/06/django-model-folder-example.png %}
Estaba yo aquí con mi insomnio habitual (¡y sin café de por medio!) trasteando con django un poco cuando me he dado cuenta de que mi ficherico _models.py_ se me estaba haciendo <del>algo</del> muy incómodo de mantener, y yo que estaba pensando un poco que python es muy _másmola_ y tal. Alguna manera ha de haber de mejorar esta cosa.

Pues bien, después de indagar un poco por internet y demás, ver algunas listas de correo he encontrado algo que me resulta bastante cómodo.

Pues bien, en mi caso dentro de la carpeta de mi app he creado otra llamada **model** -tengo la costumbre de usar la nomenclatura en singular-, y ahí un fichero .py por cada modelo y a su vez el modelo de la zona de administración.

¿Cómo hacemos funcionar bien algo así? Bien, primero en el _Meta_ de nuestro modelo tenemos que añadir el app_label. Por defecto, django usa el nombre del paquete (HAHAHAHAHA) en el que están los modelos como etiqueta de app por defecto, por lo que como he metido los mios en un paquete llamado "model", usa eso de app_label, por lo que manualmente le he especificado el correcto:

``` python item.py
class Item(models.Model):
    #...
    name = models.CharField(max_length=32)

    class Meta:
        app_label = 'database'
        ordering = ['name']
```

A su vez, en el `models.py` incluímos todos nuestros modelos: `from model import *`

Y para que esto funcione, hay que configurar nuestro paquetillo _models_ e incluir en el todos los modelos que queramos que se autoimporten, por lo que así lo especificamos en nuestro **APPNAME/model/__init__.py**:

``` python app/model/__init__.py
from database.model.version import Version
from database.model.icon import Icon
from database.model.item import Item
 
 __all__ = ['Version', 'Icon', 'Item']
```

Mucho más simple de mantener que todo en el mismo fichero. La verdad que lo he agradecido mucho, espero que os sirva de ayuda.
