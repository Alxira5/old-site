---
layout: post
title: Como crear y configurar un aviso de cookies en Blogger
description: En este tutorial, te enseñaré cómo convertir una imagen en un favicon funcional en Blogger.
image: 
  path: /old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/aviso-de-cookies.png
  alt: Aviso de cookies
permalink: /blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/
---

> Publicación original: [Wayback Machine](https://web.archive.org/web/20220903073358/https://machibitothegamer.blogspot.com/2022/09/como-configurar-un-aviso-de-cookies-en.html)

Si queremos monetizar nuestro sitio web necesitamos un aviso de cookies, si
queremos analizar nuestro sitio web necesitamos un aviso, bueno para todo
necesitamos un aviso de cookies ya que es la ley, bueno precisamente la GPDR,
porque los administradores de sitios web debemos informarle a los visitantes
que el sitio web utiliza las cookies de su navegador web para dichos
propósitos. En este tutorial vamos a configurar un aviso de cookies tipo
banner, como pueden ver en la imagen anterior, aunque sé que es un aviso de
cookies sencillo pero cumple su función de avisarle a los usuarios que el sitio
web utiliza cookies, bueno ya basta de hablar y empecemos con el tutorial.

## Antes de empezar

![Video de YouTube](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/video-de-youtube.jpg)

Recuerda que si no entiendes los pasos que colocare a continuación, puedes ver
el tutorial en el
[video](https://web.archive.org/web/20220901004539/https://www.youtube.com/watch?v=X0BM_1FRScU)
que coloque en esta seccion.

## Paso 1: Ir a diseño

![Diseño](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/diseno.png)

La única forma de configurar el aviso de cookies es en diseño, para los que se
pregunten porque lo vamos a configurar en diseño y no en temas y edito el
código HTML de mi sitio web, bueno realmente les quiero decir que lo intente y
no me funciono, así que la única manera de configurarlo es en diseño.

## Paso 2: Seleccionar "Agregar un gadget"

![Agregar un gadget](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/agregar-un-gadget.png)

Una vez que vayamos a diseño obviamente no se va configurar el aviso de cookies
automáticamente, bueno una vez estemos en diseño solo faltaría seleccionar
"Agregar un gadget".

## Paso 3: Seleccionar "HTML/JavaScript"

Para agregar el aviso de cookies en nuestro sitio web hay que seleccionar
"HTML/JavaScript" para colocar el código del aviso de cookies.

## Paso 4: Copiar y editar el código

![Código](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/codigo.png)

Esta es la parte más importante del tutorial, una vez abierto la ventana de
configuración del gadget, copiamos el código del aviso de cookies, recuerda que
puedes modificar las secciones marcadas con el color azul, y una vez terminado
de editar el código pulsamos en "Guardar".

## Paso 5: Mover el aviso de cookies al final del "Cuerpo de la página"

![Mover el gadget](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/mover-el-gadget.png)

Al igual que el paso anterior, este paso es muy importante ya que si lo dejamos
en la barra lateral, lo cual es donde se ubica por defecto, solo aparecerá
cuando abramos la barra lateral del sitio web, entonces seria como si no
hubiera un aviso de cookies. Entonces por eso es muy importante moverlo al
final del cuerpo de la página.

## Paso 6: Guardar la configuración

![Guardar](/old-site/assets/images/blog/como-crear-y-configurar-un-aviso-de-cookies-en-blogger/guardar.png)

Este sería el último paso de este tutorial, y el más fácil, ya que solo nos
queda guardar la configuración para que tenga efecto.

Una vez guardado la configuración, el aviso de cookies aparecerá de manera
inmediata en nuestro sitio web, les recomiendo que si quieren ver cómo les
quedo pueden utilizar una ventana de incognito.

## Código

El código del aviso de cookies puedes encontrarlo a continuación, recuerda que
las secciones que puedes modificar están marcadas con el color azul:

```html
<div id="barracookies">
El sitio web Machibito the Gamer utiliza cookies propias y de terceros para poder hacer análisis y personalizar su experiencia
<br/>
Si continúa utilizando el sitio web consideraré que acepta su uso <a href="javascript:void(0);" onclick="var expiration = new Date(); expiration.setTime(expiration.getTime() + (60000*60*24*365)); setCookie('avisocookies','1',expiration,'/');document.getElementById('barracookies').style.display='none';"><b>Entendido</b></a> <a href="https://machibitothegamer.blogspot.com/p/uso-de-cookies.html" target="_blank" >Más información</a>
</div>
<!-- Estilo barra CSS -->
<style>#barracookies {display: none;z-index: 99999;position:fixed;left:0px;right:0px;bottom:0px;width:100%;min-height:40px;padding:5px;background: #696969;color:#FFFFFF;line-height:20px;font-family:verdana;font-size:12px;text-align:center;box-sizing:border-box;} #barracookies a:nth-child(2) {padding:4px;background:#4682B4;border-radius:5px;text-decoration:none;} #barracookies a {color: #fff;text-decoration: none;}</style>
<!-- Gestión de cookies-->
<script type='text/javascript'>function setCookie(name,value,expires,path,domain,secure){document.cookie=name+"="+escape(value)+((expires==null)?"":"; expires="+expires.toGMTString())+((path==null)?"":"; path="+path)+((domain==null)?"":"; domain="+domain)+((secure==null)?"":"; secure")}function getCookie(name){var cname=name+"=";var dc=document.cookie;if(dc.length>0){begin=dc.indexOf(cname);if(begin!=-1){begin+=cname.length;end=dc.indexOf(";",begin);if(end==-1)end=dc.length;return unescape(dc.substring(begin,end))}}return null}function delCookie(name,path,domain){if(getCookie(name)){document.cookie=name+"="+((path==null)?"":"; path="+path)+((domain==null)?"":"; domain="+domain)+"; expires=Thu, 01-Jan-70 00:00:01 GMT"}}</script>
<!-- Gestión barra aviso cookies -->
<script type='text/javascript'>
var comprobar = getCookie("avisocookies");
if (comprobar != null) {}
else {
var expiration = new Date();
expiration.setTime(expiration.getTime() + (60000*60*24*365));
setCookie("avisocookies","1",expiration);
document.getElementById("barracookies").style.display="block"; }
</script>
```

## Referencias

Código del aviso de cookies: [Bloggin Red](https://web.archive.org/web/20230208034414/https://www.blogginred.com/2016/08/poner-aviso-de-uso-de-cookies-en-blog.html)
