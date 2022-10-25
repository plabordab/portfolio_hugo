<h1 align="center"> PROYECTO HUGO </h1>

## Índice

[Descripción del proyecto](#descripción-del-proyecto)

[Estado del proyecto](#Estado-del-proyecto)

[Características de la aplicación](#Características-de-la-aplicación-y-demostración)

[Acceso al proyecto](#acceso-proyecto)

[Tecnologías utilizadas](#tecnologías-utilizadas)

[Conclusión](#conclusión)

## Descripción del proyecto

Este proyecto consiste en crear un sitio estático con HUGO. Para realizarlo he seleccionado el tema "UNIVERSAL", está más orientado a la creación de un blog, pero me gustaba mucho el diseño y por eso decidí utilizarlo.

## Estado del proyecto

El proyecto se encuentra finalizado, con los contratiempos con los que me he encontrado por falta de funcionalides del tema 'Universal' al no poder incluir la selección de idiomas y la no visualización de los canales de televisión.

## Características de la aplicación

#### Página de inicio

Dispone de un carrusel donde se muestra de manera automática diferentes imágenes y su descripción, relacionado con el contendido que voy a desarrollar.

Debajo del carrusel se encuentran dos elementos incluidos en la sección _features_ con sus accesos directos correspondientes.

A continuación se muestra otra sección, cuyo enlace nos lleva a la visualización de canales de televisión.

Al final, se muestra la información de contacto y un enlace para ir a dicha página.

#### Página de contacto

En esta sección, además de incluir información sobre mí, he habilitado el formulario de contacto.

Intenté habilitar la opción del captcha de google, pero no me permitía el dominio: 'https://plabordab.github.io/portfolio_hugo'

#### Menú

El menú superior, además del enlace a "Sobre mí" tiene una opción con un desplegable que incluye los siguientes manuales que voy a explicar:

| HUGO | GIT | DOCKER | 
| --- | --- | --- |
| Instalación | Git Init | Instalación |  
| Configuración | Git Push | Configuración |  
| Tema Universal | Git Pull | Apache |  
| Markdown | |  |  

#### Menú superior de shortcodes sociales

El menú de shorcodes superior tiene los siguientes accesos directos a mis correspondientes cuentas, con sus respectivos iconos:

- GitHub
- Linkedin
- Email

#### Idiomas

Me ha surgido un problema a la hora de incluir la selección del idioma y, finalmente, con este tema no he conseguido utilizar esta función.

#### Gráficos mermaid

Según la [documentación oficial de Hugo](https://gohugo.io/content-management/diagrams/#mermaid-diagrams), el programa no proporciona, actualmente, plantillas por defecto para los diagramas Mermaid. 

Pero explica que se pueden crear unas propias fácilmente escribiendo el siguiente fragmento de código en el directorio: `layouts/_default/_markup/render-codeblock-mermaid.html`:

```js
<div class="mermaid">
  {{- .Inner | safeHTML }}
</div>
{{ .Page.Store.Set "hasMermaid" true }}
```

Y después incluir en la parte inferior de la plantilla de contenido (debajo de .Content, ya que el gancho de renderización no se procesa hasta que se ejecuta .Content).

```js
{{ if .Page.Store.Get "hasMermaid" }}
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
  <script>
    mermaid.initialize({ startOnLoad: true });
  </script>
{{ end }}
```

En concreto, lo he incluído al final de `layouts/partials/footer.html`:

#### Datos externos

Me parecía una idea muy buena incluir la parrilla de canales televisivos en mi página web, y así, poder consumir datos desde un fichero `json`.

A pesar de mis buenas intenciones, siguiendo los pasos incluidos en el manual, no he conseguido que mi sitio muestre los canales; no sé si trata de otro problema de compatibilidad con mi tema seleccionado, ya que he seguido el mismo procedimiento en otro proyecto y no he tenido problemas.

## Acceso al proyecto

La URL del proyecto es: https://plabordab.github.io/portfolio_hugo.

## Tecnologías utilizadas

Principalmente, he utilizado el lenguaje Markdow para explicar otras tecnologías como HUGO, GIT o DOCKER.

## Conclusión

Me decanté por este tema, principalmente, por el carrusel; ya que me parece una idea fantástica para expresar a golpe visual un resumen del contenido de mi página web sin que el usuario necesite hacer scroll.

Además, el menú es simple pero completo y facilita, con las subsecciones, la búsqueda de la información a consultar.

También dispone de fácil acceso los enlaces de contacto, algo que me parece muy importante para un portfolio, igual que el formulario de contacto.

Seguiré trabajando con este tema, ya que tiene otras muchas posibilidades, aunque no se adaptaban a las características de mi proyecto actual.

Hugo me ha parecido una aplicación muy popontente, con muchas posibilidades para crear un sitio estático.

En conclusión, esta página web tiene una navegación muy simple y visual, ofreciendo una gran usabilidad para la interacción de los usuarios. 