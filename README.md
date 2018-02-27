# TAREA-3-4-Y-5

## EXAMEN CON AUTOCORRECCIÓN
-He realizado una aplicación web de examen con autocorrección muy ligera, poco más de 100 kb en total, gracias al uso mínimo de gráficos y aprovechando los estilos css.
La aplicación web consta de las siguientes partes:

### Carpeta principal:
-index.html: es la página principal, contiene una serie de instrucciones para realizar el examen y un botón que enlaza a la página del examen.

-examen.html: es la página del examen, muestra las preguntas y una vez corregido el examen muestra también las respuestas correctas, así como un temporizador de 10 minutos para hacer el examen, los fallos cometidos y la nota final.
Al acabar el examen y su corrección, se puede volver a intentar el examen con un botón que lo reinicia.
He incluido un pequeño pop up en la parte superior de la página para recordar las instrucciones durante el examen.

### Carpeta css
Cuenta con dos hojas de estilos css, una para pantallas grandes y otra para pantallas pequeñas.

-d.css: pantallas grandes.

-m.css: pantallas pequeñas.

### Carpeta img:
Cuenta con dos imágenes, una de ellas es el banner que aparece en la cabecera de la página y un favicon. Ambas optimizadas con Photoshop para conseguir el menor tamaño de archivo posible.

### Carpeta js:
En la carpeta js tenemos dos archivos:

-code.js: es el código JavaScript que hace que el examen funcione.

-Preguntas.json: archivo generado automáticamente a partir del archivo code.js con una herramienta online.

### Carpeta XML:

-preguntas.dtd: para validar el fichero preguntas.xml.

-preguntas.xml: contiene las preguntas y las respuestas del examen.

-preguntas.xsd: archivo generado a partir de preguntas.xml con una herramienta online.

-preguntas.xsl: es el archivo que hace que las respuestas del .xml se muestren en el examen.html.

### Componentes de la aplicación

-Pop-up: muestra un pequeño pop-up que se puede cerrar haciendo click en el o sobre el botón del mismo.
Por motivos de diseño, he suprimido el pop-up en la versión para pequeñas pantallas.
El código que hace que funcione el pop-up es el de la línea 666 a la 668 del archivo code.js.


-Temporizador: el temporizador funciona gracias al código de la línea 40 a la 57 del code.js.
El temporizador empieza en 10 minutos, a partir de ahí, se le indica que vaya restando 1 segundo cada segundo (expresado en milisegundos).
Cuando se agota el tiempo muestra un alert avisando de que se ha acabado el tiempo, esto hace que el examen se corrija directamente tal y como está en el momento de agotarse el tiempo.
Si el usuario no agota el tiempo y le da a corregir, el temporizador se detiene.


-Formulario: a partir de la línea 38 hasta la 117 están las preguntas del examen.
10 preguntas de 5 tipos diferentes.
Preguntas 1 y 2: text.
Preguntas 3 y 4: radio.
Preguntas 5 y 6: select multiple.
Preguntas 7 y 8: select.
Preguntas 9 y 10: checkbox.


-Botón de corrección del examen: simplemente es el botón que acciona el código JavaScript necesario para corregir el examen.
Al pulsar este botón, se pide confirmación para proceder con la corrección del examen. Después, el código comprueba si todas las respuestas están contestadas, si no lo están, devuelve un mensaje indicando que preguntas faltan (indica la primera pregunta sin responder) y no deja corregir el examen.
Si el examen está rellenado completamente, devolverá las preguntas y respuestas del archivo preguntas.xml.
Además, indicará al usuario en que se ha equivocado.
La corrección funciona perfectamente en Firefox, en Chrome, corrige, pero su aspecto no es del todo el esperado. No he conseguido saber muy bien cuál es el problema aquí, pero, de todas formas, el examen también corrige en Chrome.
Finalmente da una nota que se hace a partir de la suma de los diferentes aciertos en las 10 preguntas.


-Botón de volver a intentar: este botón se desbloquea solo cuando se ha corregido el examen. Reinicia el examen.

En el archivo code.js, están comentadas las diferentes partes del código, donde se explica cada apartado del mismo.
En las hojas de estilos .css también hay comentarios explicando los diferentes estilos.

### Otros: 
-En el formulario he visto que al poner un select multiple, para seleccionar varias opciones hay que hacer control + click, puesto que he visto que no todo el mundo sabe que se puede seleccionar de esta forma, he decidido implementar un código, que empieza en la línea 652 hasta la 663 del archivo code.js, que lo que hace es marcar las opciones sin la tecla control, solo haciendo click.


-He compartido la página de RawGit en Facebook y he puesto las etiquetas meta en el head del index.html.

### Validación:

### HTML

-index.html: https://goo.gl/SLSsA7

-examen.html: https://goo.gl/eBSXiJ

### CSS
-d.css: https://goo.gl/ZCQtqi

-m.css: https://goo.gl/6PeXVW

### RESTO DE ARCHIVOS
-He creado el archivo .xsd a partir del .xml en esta página: https://goo.gl/2DeV4B

-He validado el documento: https://goo.gl/GrC8Mg

-He creado el archivo .json a partir del .xml en esta página: https://goo.gl/556uBE
