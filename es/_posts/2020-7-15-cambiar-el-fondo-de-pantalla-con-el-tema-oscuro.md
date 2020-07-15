---
title: Cambiar el fondo de pantalla con el tema oscuro
i18n-link: theme-sensitive-wp-automate
---
La mayor parte del tiempo uso el tema oscuro en mi teléfono, pero aveces (generalmente cuando estoy fuera) necesito desactivarlo para ver qué hay en mi pantalla.

Pero recientemente me di cuenta que esto no es suficiente porque el fondo de pantalla sigue siendo demasiado oscuro para ver las aplicaciones en el launcher.
La solución es obvia: _cambiar el fondo de pantalla cuando activo o desactivo el modo noche_.

<!--more-->

Primero pensé que ya habría alguna app que hiciera esto automáticamente.
[Al parecer, existe](https://play.google.com/store/apps/details?id=com.cannic.apps.automaticdarktheme), pero esta es solo una función secundaria, y no me gusta tener 2.000 apps aparte para cada pequeña función que quiera añadir.

Después recordé otra aplicación más útil llamada [Automate](https://play.google.com/store/apps/details?id=com.llamalab.automate).
Si bien esta también puede hacer más que solo cambiar una imagen de fondo, no es un problema porque ese no es el único uso que le voy a dar.
Además, Automatic Dark Theme no me permite cambiar el fondo de la pantalla de bloqueo `¯\_(ツ)_/¯`

Al final hice un flow bastante sencillo:

<img
	src="{{ page.blog-media }}/{{ page.i18n-link }}/flow.png"
	class="float"/>

- Espera a que cambie el tema del sistema
  - Si se activó el modo oscuro, pone fondos de pantalla oscuros
  - Si no, pone fondos claros
- Repite indefinidamente

Así se ve:
<video controls>
	<source
		src="{{ page.blog-media }}/{{ page.i18n-link }}/demo.webm"
		type="video/webm">

	<p>Tu navegador no soporta archivos WebM. Por favor, <a href="{{ page.blog-media }}/{{ page.i18n-link }}/demo.webm">descargá el archivo</a> y abrilo con tu reproductor favorito.</p>
	<small><i>Tomá una moneda. Conseguite un navegador mejor.</i></small>
</video>

Si querés usar este Flow, seguí estos pasos:
1. Descargá el [archivo](https://mega.nz/file/jQkBiQJL#lG6rRVFWttmH0X_X66d5yz_3cyxnN0F8r3JoZHnPWoU) a tu teléfono.
2. Descargá [Automate](https://play.google.com/store/apps/details?id=com.llamalab.automate).
3. Cuando lo hayas instalado, abrí Opciones ➡ Importar y seleccioná el archivo.
4. Seleccioná el item "Theme-sensitive wallpaper", clickeá el botón de Editar y abrí el editor de flows.
5. Abrí cada bloque de _"Set image wallpaper"_ y clickeá la ▼ para seleccionar cada imagen
(**NOTA:** La imagen debe estar ya recortada a tu gusto)
6. Para terminar, salí del editor y clickeá el botón de inicio.

Si no querés cambiar el fondo de la pantalla de bloqueo, solo hace falta borrar los últimos dos bloques.

Y eso sería todo.
Ahora, cada vez que cambies el tema del sistema, tu fundo de pantalla va a cambiar también.
Genial, no? 😄
