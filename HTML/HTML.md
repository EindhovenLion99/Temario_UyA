# Introduccion a HTML

# HTML

* HTML es un lenguaje de marcas para definir la estructura de hipertexto de un documento.
* Es un estándar definido por el W3C, lo que garantiza que una misma página sea visualizada de forma muy similar en cualquier navegador o S.O.
* El W3C aprobó en 2014 la definición del estándar HTML5.
* XHTML es una versión avanzada de HTML basada en XML.

# Sintaxis básica HTML

Etiquetas:
```html
<Nombre> Contenido </Nombre>
```
Todo el documento estará marcado por la etiqueta 
``` html
<html> Documento </html> 
```
Partes de un documento HTML:
> * Cabecera contiene el título e información relativa al propio documento. El usuario sólo verá la información del título.
> * Cuerpo contiene la información que se mostrará en el navegador

# Documento HTML
```html
<html>
    <head>
        Cabecera
    </head>
    <body>
        Cuerpo
    </body>
<html>
```

# Etiquetas, atributos, elementos.

Los elementos son las partes del documento HTML. Están formados por:

> * Etiquetas Marcan los elementos
> * Texto o contenido del elemento
> * Atributos Especifican información adicional

Los elementos pueden ser
> * en línea: sólo ocupan el espacio necesario
> * en bloque: siempre empiezan en una nueva línea y ocupan toda la línea

Cada etiqueta tiene un conjunto de atributos que se le pueden aplicar.
```html
<a title="Saltar índice" href="#a">Saltar índice</a>
```
> * Hay atributos básicos, de internacionalización, de evento, de foco.

# Estructurar texto

El texto se puede estructurar en:

> * Párrafos
```html
<p> Texto </p>
```
> * Secciones jerárquicas, admite hasta 6 niveles:
```html
<h1> Título sección</h1> <h4> Título sección </h4>
<h2>Título sección</h2> <h5> Título sección </h5>
<h3> Título sección</h3> <h6> Título sección </h6>
```

# Entidades

> * La presentación al usuario de caracteres que no corresponden al idioma inglés: ñ, á, é, í, ó, ú, etc. puede generar problemas si no se utiliza la misma codificación en todo el proceso.
> * Caracteres reservados para la sintaxis de html
> * Las entidades representan de forma inequívoca todos estos caracteres.

# Marcar texto

* Enfatizar:
```html
<em> Texto </em> <strong> Texto </strong>
```
> * Asi quedaria: <em> Texto </em> <strong> Texto </strong>

* Espacios en blanco, se ignoran salvo que se especifique
```html
&nbsp
```
* Nueva línea 
```html
<br>
```
* Otras etiquetas permiten usar abreviaturas, acrónimos, citas, definiciones, etc..
```html
<abbr> <acronym> <dfn>
```

# Enlaces
```html
<a> Texto </a>
``` 
> * El navegador carga los recursos enlazados con esta etiqueta cuando el usuario pincha sobre ellos.
* Atributos: 
* * href = “URL del recurso enlazado” 
* * name = “texto para definir enlaces dentro de la misma página.” 
* * rel  = Relación con la página enlazada 
* * rev  = Relación de la página enlazada con la página actual 
* * charset = “codificación utilizada”

* Relaciones entre páginas: alternate, stylesheet, start, next, prev, contents, bookmark, ...
* Codificación: UTF-8, ISO-8859-1

* Enlaces que se cargan automáticamente:
```html
<script> </script> 
```
Puede ser un enlace a un fichero con código, generalmente JavaScript o incluir el códigodirectamente. 
* Atributos

> * src = “url del fichero con el código”
> * charset = “codificación de caracteres usada en el código”
> * type = “tipo de código, generalmente JavaScript” 
```html
<link Atributos/> 
```
Se enlazan generalmente hojas de estilo, favicon, hojas de estilo para diferentes medios, páginas preparadas para imprimir, etc. Siempre va en la sección head.
> * Atributos: href, hlang, type, charset, rel, rev, media puede ser screen, print, handled

# Listas

* Listas no ordenadas:
```html
<ul>
    <li> Elemento 1 </li> 
    <li> Elemento n </li>
</ul>
```
* Listas ordenadas:
```html
<ol>
    <li> Elemento 1 </li> 
    <li> Elemento n </li>
</ol>
```


# Imágenes

```html
<img Atributos/>
```
* Atributos:
> * src = “url de la imagen”. Se aconsejan los formatos png, jpg, gif.
> * alt = “texto” Descripción corta 
> * longdesc = “texto” Descripción larga 
> * name = “texto” Nombre de la imagen 
> * width = “ancho” Se puede expresar en % del tamaño del contenedor 
> * height = “alto” Se puede expresar en % del tamaño del contenedor

# Tablas
```html
<table>

    <tr> <!--Fila1-->

        <td>Celda11</td> <td>Celda12</td> <td>Celda13</td>

    </tr>

    <tr> <!--Fila2-->

        <td> Celda21</td> <td> Celda22</td> <td> Celda23</td>

    </tr>

</table>

<caption> Título </caption>
```

* Atributos 
```html
<table summary =“texto”>
```
> * Descripción del contenido.
```html
<td Abbr = “texto”
    Headers= id_celda_cabecera
    Scope = "col, row, colgroup, rowgroup"
    Colspan =“numero” 
    Rowspan = “numero” >
```
> * Número de columnas que ocupa la celda (Colspan)
> * Número de filas que ocupa la celda (Rowspan)

# Formularios
```html
<form> 
</form>
```
> * action = “url” 
> * method = GET, POST 
> * enctype = “codificación usada al enviar los datos al servidor” 
> * accept = “lista de tipos de archivos aceptados por el servidor”

Los elementos del formulario se marcan con la etiqueta ```<input>```
* Atributos: 
> * type = "text | password | checkbox | radio | submit | reset | file | hidden | image | button” 
> * value = “texto” Valor inicial 
> * src = “url” url de la imagen en los botones

* Agrupar elementos
```html
<fieldset> Grupo </fieldset> 
<legend> Título del grupo </>
```
* Nombre de los elementos del formulario
```html
<label> Nombre </label>
```
Otros elementos:

* Áreas de texto: ```<textarea>``` 
* Listas desplegables:
```html
<select>
    <option> Opcion1 </option>
    <option> Opcion2 </option>
</select>
```

# HTML5

Elementos eliminados: 
```html
<acronym>, <applet>, <object>, <basefont>, <big>, <center>, <dir>, <ul>, <font>, <frame>, <frameset>, <noframes>, <strike>, <tt>
```
Nuevos elementos: 
* Semánticos: 
```html
<header>, <footer>, <article>, <section>. 
```
* Gráficos: 
```html
<svg>, <canvas>.
```
* Multimedia: 
```html
<audio> and <video>.
```
* Nuevos atributos: 
```html
number, date, time, calendar, and range
```

# Tipos de documentos

HTML5
```html
<!DOCTYPE html>
```
HTML4 Strict
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```
HTML4 Transitional
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

XHTML4 Strict
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

XHTML4 Transitional
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```