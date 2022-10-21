---
title: "Git"
date: 2022-09-27T19:54:33+02:00
draft: false
---

# REPOSITORIO EN GITHUB

## crear un repositorio nuevo y ligarlo al local

1. Accedemos a github con nuestro usuario y password
2. En nuestra cuenta creamos un repositorio
3. Nos muestra los comando a ejecutar en local. Las acciones son:
4. Vamos a local al directorio donde está nuestro proyecto
5. Ejecutamos: 

a.

```
git init 
```
>  este comando inicializa nuestro directorio como un poryecto de git. Habrá creado un directorio llamado .git


b. 

```
git add . 
```
>  con este comando añadimos los ficheros de mi directorio (todos por especificar .) al repositorio


c.

```
git comit -m "mensaje de checkpoint" 
```
>  con este comando especificamos un mensaje para los cambios actuales


d. 

```
git branch -M main 
```
>  con este comando creamos una rama o directorio de trabajo asociado al repositorio local


e.

```
git add remote origin https://github.com/plabordab/ej_hugo 
```
>  con este comando ligamos el repositorio local al remoto

f.

```
git push origin main  
```
>  con este comando sumimos los ficheros añadidos al remoto


## copiar un proyecto en otro destino

1. Accedo a git hub y copio la url del repositorio
2. Escribo:

```
git clone https://github.com/plabordab/ej_hugo 
```
> creará un directorio con el nombre del proyecto y todo el contenido (sólo se hace la primera vez)


3. Me descargo también el tema

4. Después de trabajar, para guardarlo hacemos un push:

```
git add *
git commit -m "nuevos cambios"
git push -u origin main  
```
>  actualizaré el proyecto en github con los últimos cambios


### Actualizando un proyecto modificado en otro lugar

```
git pull  
```
>  actualizo el proyecto de local con el remoto

