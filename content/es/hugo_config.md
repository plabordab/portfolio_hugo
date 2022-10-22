+++
title = "CONFIGURACIÓN DE HUGO"
tags = ["hugo"]
categories = ["hugo"]
description = "Configuracion HUGO"
banner = "img/banners/hugo.jpeg"
authors = ["Pilar Laborda"]
+++


[HUGO](https://gohugo.io/) es un programa gestor de contenido estático. 

Los sitios web estáticos no tienen base de datos, pero utilizando un API, pueden utilizar un servicio para acceder a otro.

A través de Hugo, crearemos una estructura de carpetas, junto con un fichero *****config.toml***** o *****.yaml*****.

En este fichero incluiremos los parámetros oportunos estableciendo parejas variable-valor.

En la carpeta *****content***** incluiremos ficheros de texto con extension .md.

Markdown es un lenguaje simple que se utiliza para crear texto enriquecido con un editor de texto sin formato. Permite darle un formato básico al texto, utilizando símbolos conocidos y accesibles en todos los teclados. 

> Puede consultar más información en la sección [Markdown](/hugo_md/).

Cada tema de Hugo tiene diferentes características y, por consiguiente, diferente configuración.

> En este apartado vamos a ver las generalidades, para consultar la información específica del tema seleccionado recomendamos visitar la página [Tema Universal](/hugo_tema/).

Algunas plantillas, generan los archivos de la carpeta content como borradores, para que se puedan visualizar en el sitio, será necesario cambiar el valor `draft = false`.

Se podría arrancar el servidor de desarrollo de Hugo para que muestre los archivos en borrador `draft = true` con el comando: 

``` js
hugo server -D
```

Es interesante incluir tanto un menú como algunos accesos directos que permitan realizar una navegación más usable en nuestro sitio web. 

También es importante utilizar la función de multilenguaje, pero no todos los temas disponen de ella, como es el caso del "Universal".

Todas estas configuraciones se realizan en el archivo *****config.toml*****.


#### **Publicación del sitio en Github**

Para realizar un despliegue del sitio en Github es necesario:

- Crear un repositorio en GitHub
- Hacer el commit, para confirmar los cambios del sitio web en tu repositorio local
- Asociar el repositorio local con el repositorio remoto que has creado en Github
- Sincronizar el contenido del repositorio local hacia remoto 

> Puedes consultar esta información en la sección [Subir](/git_up/).

Una vez publicado el sitio en el repositorio remoto, usar GitHub para alojar el sitio web gratuitamente es tan sencillo como ir a la configuración del repositorio de Github (settings) y seleccionar que vamos a desplegar GitHub en el directorio "docs".

Para que las rutas nos funcionen **no se nos puede olvidar cambiar la URL** del sitio web en la configuración del proyecto, archivo *****config.toml*****. 

Dado el nombre de la URL que nos proporciona GitHub, el sitio web estará configurado del siguiente modo:

``` js
baseURL = 'https://plabordab.github.io/portfolio_hugo'
```

Luego volvemos a generar el sitio completo:

``` js
hugo -d docs
```

Y hacemos el commit y push para enviarlo de nuevo a Github. 