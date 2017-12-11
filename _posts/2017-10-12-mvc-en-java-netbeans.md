--- 
layout: post 
current: post 
cover: assets/images/posts/mvc-en-java-netbeans.jpg 
navigation: True 
title: Una aproximación al patrón MVC en Java (usando Netbeans)
date: 2017-09-09 10:00:00 
tags: tutorial java
class: post-template 
subclass: 'post tag-maratones' 
author: krthr 
categories: krthr
---

Desde que sumergí en la programación con Ruby, específicamente con Ruby on Rails, la idea del patrón MVC (Modelo-Vista-Controlador) ha rondado en mi cabeza. Realmente facilita muchísimo el desarrollo, además, permite una estructuración muy organizada y fácil de entender de cualquier proyecto que estemos programando.

Así que me propuse llevar éste pratón a casi todos los entornos de programación donde me encuentre. En esta oportunidad: Java. Sí, ¡Java! D: Veamos…

## NetBeans
Para programar en Java siempre he usado NetBeans. Es un IDE estable, diseñado especialmente para el desarrollo en Java (y todo lo que se derive de esto).

## MVC
> Si no sabes acerca del Modelo-Vista-Controlador te invito a leer sobre esto. De todos modos, no es necesario saber mucho sobre el tema para entender el proyecto que aquí desarrollaré.

![](https://basicsofwebdevelopment.files.wordpress.com/2015/01/mvc_role_diagram.png)

Básicamente, la idea del MVC es separar el código de las vistas de toda la lógica de nuestra aplicación. Así mismo, separamos los módulos que sirven los datos que guardamos. ¿La has pillado? Calma, al principio puede parecer confuso - pero cuando lo entiendes será glorioso.

La cosa va así, crearemos tres paquetes en el proyecto:

- **Controllers:** Todo el código que realizará la lógica de nuestro programa. Prácticamente, el código que lleva a cabo todo lo importante de nuestro programa.
- **Models:** Los modelos son la abstracción. Ejemplo: En un programa para una droguería los modelos serían, por decir: `Cliente.java`, `Producto.java`, `Factura.java`, etc.
- **Views:** Y las vistas, como se puede deducir, es lo que el usuario verá (los formularios, ventanas, etc.)