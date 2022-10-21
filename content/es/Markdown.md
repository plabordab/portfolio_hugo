---
title: "Markdown"
date: 2022-09-23T16:59:13+02:00
draft: false
---

# h1 Título 1
## h2 Título 2
### h3 Título 3
#### h4 Título 4
##### h5 Título 5
###### h6 Título 6

<!--
comentario
-->

Cualquiera de los textos que no empiecen por un signo especial se escribirá como texto normal, sin formato, y se envolverá dentro de las etiquetas <p></p> en el HTML renderizado.

**negrita**

_cursiva_

*cursiva*

*****negrita y cursiva*****

~~tachado~~

~~***Tachado, Negrita y Cursiva***~~

> Para incluir citas 
>
>> Se puede incluir citas dentro de citas
> 
> Y continuar en la anterior

*Notas al pie de página:*

Este año visitaremos la Giralda[^1]. Será una visita importante.

*Definición de abreviaciones:*

El TAS aprobó su solicitud.

*[TAS]: Tribunal de arbitraje del deporte.

A partir de estos momentos siempre que escribamos TAS tendremos su definición disponible.

*Definición de palabras:*

Markdown
: Es un lenguaje de marcado ligero creado por John Gruber
: Es una palabra inglesa que significa reducción de precio.

#### **listas**


* enumeración 1
    - enumeración 2
        + enumeración 3

1. Listas
4. donde
2. el
12. orden
8. no
99. es
21. importante

..

1. Si sólo utiliza 1. 
1. para cada número, 
1. Markdown numerará automáticamente 
1. cada elemento

#### **Código**

Para resaltar código dentro de una frase: `sudo apt install libreoffice`.

Para incluir sangrías ponemos al menos dos espacios:
    line 1 of code
    line 2 of code
    line 3 of code


``` 
Usamos las comillas para escribir 
varias líneas de código
```

Para resaltar la sintaxis, añadimos la extensión de archivo del lenguaje que se desea utilizar después de las comillas.

```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```



#### **Tablas**

| Hora | Lunes | Martes | Miércoles | Jueves | Viernes|
| ------: | ------ | ------ | ------ | ------ | ------ | 
| 1 | Cliente | Despliegue | ------ | Cliente | Servidor | 
| 2 | Cliente | Despliegue | ------ | Cliente | Servidor | 
| 3 | Cliente | Servidor | Interfaces | Cliente | Servidor | 
| 4 | Interfaces | Servidor | Interfaces | Servidor | Interfaces | 
| 5 | Despliegue | Servidor | ------ | Servidor | Interfaces | 
| 6 | Despliegue | ------ | ------ | Servidor | Interfaces | 

Se justifica el texto a la derecha poniendo : a la derecha de los guiones de la columna correspondiente

**Listado de tareas 14-12-2019**

- [X] llevar los niños a natación
- [X] aprender markdown
- [ ] renovar mi suscripción del gimnasio


#### **Hipervínculos**

[Sintaxis Markdown](https://geekland.eu/aprender-markdown-en-minutos/ "Se puede añadir un globo con info de ayuda")


**Tablas de contenido con anclas al documento**

- [Listas](#Listas)
- [Código](#Código)
- [Tablas](#Tablas)
- [Hipervínculos](#Hipervínculos)


![Imagen no encontrada](/imagen/img1.jpeg "título opcional")

Entre dos secciones de texto podemos incluir una separación física. Para ello tenemos que escribir 3 guiones bajos seguidos 

___

> Importante meter en las imgénes el valor del alt (texto alternativo si no carga la imagen)
>
> Creamos en la carpeta static la carpeta imagen
>
> En la carpeta public se guarda toda la estructura a partir de la carpeta static





[^1]: Nombre que recibe la torre campanario de la catedral de Santa Maria de la Sede.