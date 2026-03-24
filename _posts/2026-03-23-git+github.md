---
layout: post
title: "¿Cómo crear un repositorio en Git y subirlo a GitHub?"
date: 2026-03-23
categories: recursos
image: assets/images/code.jpg
---

Sé que no soy la única que cuando trabaja proyectos de investigación tiene como 5 archivos distintos y cada uno es una versión mejorada de la anterior, sobre todo cuando se trabaja con códigos de programación. Al cabo de unas semanas aquello llega a ser un desastre y no sabes en qué versión hiciste qué.


Esto mismo le pasó a un tal Linus Torvald, sipi, el creador del kernel de *Linux*. Entonces, con tales capacidad de programación pensó: *¿Por qué no hacer un programa que ayude a gestionar las versiones que vamos sacando de cada documento de código?* (bueno, si yo hubiera sido él eso hubiera pensado). El caso es que así es cómo dio vida a su segundo hijo: **Git**. Justamente `Git` es un *sistema de control de versiones distribuido* (además de código libre); que traducido al español significa que es cómo si a la carpeta en la que estamos trabajando, así como a todos los archivos que contienen, les hicieramos un clon exacto, conocido como **repositorio** y en él iremos guardando el historial de modificaciones que vayamos generando.


Entonces, imagínate en lugar de tener 10 archivos diferentes, cada uno con una versión distinta del mismo código, solo tendremos un archivo y al lado el historial de los cambios que le hemos hecho. Y luego llega `GitHub`, que es una plataforma web que tiene el propósito de alojar el código que desarrolladores suben a dicha plataforma. Ofrece varias opciones, entre ellas, evidentemente tener una copia en la nube de tus archivos locales, descargar los ficheros y carpetas exactamente como el autor los coloca (es decir, clonas el repositorio lo que garantiza la reproducibilidad); además, puedes entrar a la documentación de los proyectos y leer de qué van.


Así que en la entrada de hoy, te comparto los apuntes que tengo de **cómo podemos crear un repositorio en Git** para después **subirlo a GitHub** y así crear nuestro portafolio científico, compartir con otras personas nuestros proyectos, contribuir a la ciencia o solo llevar un tracker de nuestras actividades de programación.


# Paso 1: Tener el directorio y los archivos listos
Sé que es muy obvio, pero el secreto para que nuestros proyectos científicos funcionen y no estemos perdidos a la mitad es tener una buena estructura de organización de directorios (carpetas) y ficheros (archivos). Si tu trabajo se encuentra alrededor del área de las ciencias exactas, la estructura que me ha salvado de mucho es la siguiente:


| Directorio | Función |
|-------|--------------|
|00_DOCUMENTACION| Todos los documentos que se generan en un proyecto; desde documentación técnica hasta escritos formales y PDFs con bibliografía 
|01_DATA (INPUT) | Los datos que ocuparemos de entrada y con los cuales trabajaremos
|02_SCRIPTS | Los códigos propios o que recuperamos de otros lados para el trabajo
|03_OUTPUTS | Las salidas, evidentemente, figuras, tablas, gráficos, todo lo que vayamos generando


Obviamente, todo lo anterior puede cambiarse y ajustarse a tus necesidades. Una vez que tenemos todo organizado o al menos lo más posible, debemos crear desde nuestra computadora local el archivo `README.md`. Este es un archivo super sencillo hecho en *Markdown* en el que describimos las características generales de lo que se encuentra dentro del repositorio.


# Paso 2: Crear el repositorio local


Una vez que tenemos listos nuestros archivos, procedemos a ubicarnos en el directorio del cuál queremos crear el repositorio. Esto lo haces desde una terminal de Power Shell o 


``



## Fuentes consultadas


* Fernández, Y. (2019, 30 octubre). Qué es Github y qué es lo que le ofrece a los desarrolladores. Xataka. Recuperado de https://www.xataka.com/basics/que-github-que-que-le-ofrece-a-desarrolladores en 24 de marzo de 2026.


* HolaMundo. (2022, 18 febrero). Aprende GIT ahora! curso completo GRATIS desde cero [Vídeo]. YouTube. https://www.youtube.com/watch?v=VdGzPZ31ts8


* Mijacobs. (s. f.). ¿Qué es Git? - Azure DevOps. Microsoft Learn. Recuperado de https://learn.microsoft.com/es-es/devops/develop/git/what-is-git en 24 de marzo de 2026.

