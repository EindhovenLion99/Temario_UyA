# jQuery

* Framework javascript:
> * Simplifica la manipulación del árbol DOM
> * Facilita las comunicaciones asíncronas (AJAX)
> * Se puede enlazar desde un CDN, o desde un fichero local

# Selectores

* Permiten seliecconar elementos del árbol DOM.
* Se dispone de selectores CSS y algunos propios.
* Se pueden encadenar selectores, pero el rendimiento disminuye si la cadena es muy extensa.
* Los selectores devuelven devuelven un objeto, objeto, que puede ser un único elemento o un array de elementos.
* Para comprobar si se ha obtenido obtenido elementos utilizar .length()

* Selector de etiqueta:
```
$('elementoHtml'): Devuelve la colección de elementos que corresponden a la etiqueta.
$('.miclase'): Devuelve la colección de elementos que pertenecen a miclase
$('#mid'): Devuelve el elemento mid
```

* Selectores de atributo
```
$('elemento[atributo=valor]'): Devuelve la colección de elementos "elemento" con valor del atributo igual a valor
$('elemento[atributo^=inicioatrib]')
$('elemento[atributo$=finatrib]')
$('elemento[atributo*=contieneatrib]’)
```

* Se pueden establecer combinaciones de selectores
* Por rendimiento se deben especificar selectores lo más específicos posible
* Siempre que sea posible utilizar selectores basados basados en etiquetas etiquetas, nombres nombres de clase, ids
* Si vamos a utilizar posteriormente los elementos al l macenarlos en j it avascript para no
tener que recuperarlos de nuevo

# Filtros

* Nos permiten acceder a un elementoo o subconjunto de ellos dentro de la selección definida:
```
$(‘selector : filtro’)
– :first
– :last
– :odd
– :even
– :not(condición)
```
* Selectores de formulario:
```
$(‘#formulario:selectorformulario’):
– :button
– :checkbox
– :checked
```

# Metodos setter y getter

* jQuery define para los objetos recuperados una serie de métodos sobrecargados que actúan como setter o getter:
```
$(‘elemento’).html(‘mi_contenido’)
: actúa como setter
```
```
$(‘elemento’).html() 
: actúa como getter
```

# jQuery - CSS

* Se pueden obtener obtener y establecer propiedades propiedades css:
```
$('selector').css('propiedad') getter
$('selector').css('propiedad', 'valor') setter
$('selector').css({'propiedad': 'valor1','propiedad': valor2, ...}
```
* Para lograr efectos CSS dinámicos es mejor opción definir los estilos en CSS y cambiar dinámicamente la clase que se asigna al elemento: elemento:
```
.addClass()
.removeClass()
.hasClass()
.toggleClass()
.width()
.height()
.position
.attr()
```

# Eventos

* En lugar de utilizar el atributo correspondiente en el documento se definen en jQuery
```
$(‘selemento’).evento( function(){...bloque de código})
```