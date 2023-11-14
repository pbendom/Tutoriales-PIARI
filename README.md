## Introducción

En este tutorial con Scratch veremos cómo programar el videojuego de PONG en su versión para dos jugadores. 

El videojuego consiste en hacer rebotar la pelota sin tocar los laterales de la pantalla en cuyo caso acumulará puntos para tu rival.

![](img/preview.gif "Videojuego de pong con Scratch")

### Reinventa, programa y comparte

En este caso, como el juego no lo vamos a acabar en un día, es recomendable que antes de empezar os creéis una cuenta en Scratch para que se vayan guardando los cambios realizados automáticamente.

![](img/unete.png "https://scratch.mit.edu/join") 

![](img/unete2.png "Registro con nombre de usuario y contraseña (no es necesario correo electrónico)")

- Reinventa el proyecto [Pong 2 Jugadores - https://scratch.mit.edu/projects/924537702/editor](https://scratch.mit.edu/projects/924537702/editor) para obtener todas las imágenes necesarias.

![](img/reinv.png)
![](img/reinv2.png)

<br />


## Escenario

En primer lugar, comprueba que tenemos creados 4 escenarios. 

- Los 3 primeros corresponden a la cuenta atrás antes del inicio del juego (3, 2 y 1). 

- El último escenario será la pantalla principal.

![](img/escenario1.png "escenario del videojuego")

### Programación del escenario

Creamos el evento "Inicializar" destinado al cambio de fondos en la cuenta atrás. De esta forma, siempre que invoquemos al evento "Inicializar", empezará la cuenta atrás mostrando los diferentes fondos (3, 2, 1).

![](img/pong1.gif "Evento Inicializar")

Por último, invocamos al evento "Inicializar" para que sea lo primero que se ejecute al presionar la bandera verde.

![](img/pong2.gif "Bandera verde - llamar a Inicializar")

![](img/pong1.png)

> Observar que si durante el transcurso del videojuego volvemos a invocar a la función "inicializar", los fondos volverán a cambiarse (3, 2, 1).


<br />



## Pelota

Nos dirigimos al objeto que utilizaremos como bola, y ajustamos el tamaño deseado. Además, inicializamos los valores por defecto que tomará dicho objeto. En este caso, la posición va a ser la posición 0 en el eje X y la posición 0 en el eje Y, es decir, (0,0).

![](img/pong2.png)

También le vamos a añadir un ángulo aleatorio de giro. En este caso, vamos a optar por un ángulo comprendido entre 45º y 135º para intentar que el ángulo sea lo más horizontal posible.

![](img/pong3.png)


### Programación de la pelota

Lo primero que haremos es crear un evento "Comenzar juego" dentro de la bandera verde (en el objeto escenario). Una vez lo tengamos, añadimos el bloque también a la pelota.

![](img/pong3.gif "Bandera verde - llamar a Comenzar juego")

La pelota se debe mover N pasos y rebotar si toca el borde. Para indicarle el valor N, creamos una variable llamada "Velocidad".

    NOTA: Como ya sabemos de otras prácticas, siempre que se utilizan variables debemos de inicializarlas a un valor por defecto. En este caso, le asignamos el valor en la función "Inicializar".

![](img/pong4.gif "Bandera verde - añadir variable")

Como se puede observar, la velocidad de la bola será siempre la misma. Haremos que se vaya incrementando en niveles posteriores.

![](img/pong4.png)

<br />



## Jugadores

<div class="iframe">
  <iframe src="//www.youtube.com/embed/ze-cvFf5DfE" allowfullscreen></iframe>
</div>

### Jugadores del videojuego

Mediante el editor de fondos o con ayuda de otro software extreno, creamos las palas de lo ambos jugadores, cada una de un color.

En primer lugar se inicializan las posiciones origen de cada paleta, en su eje x e y respectivamente. A continuación al recibir la llamada del evento `Comienza juego` cambiamos las posiciones de la coordenada vertical para que la paleta suba o baje según la tecla presionada.

Por último, modificamos la programación de la bola para que rebote no sólo cuando toca un borde, sino que además deberá rebotar si toca cualquiera de las paletas.

![](img/jugadores.jpg "Jugadores del videojuego")



<br />



## Mejoras

<div class="iframe">
  <iframe src="//www.youtube.com/embed/qYQzBsWAmhU" allowfullscreen></iframe>
</div>

### Mejoras aplicadas al videojuego

Se crean 2 variables donde almacenaremos los puntos de cada jugador. De este modo cada vez que la bola toque un borde opuesto al jugador, este sumará 1 punto. Para detectar dichos bordes, nos ayudamos de las coordenadas sobre el eje horizontal X, detectando si el valor de X es menor o igual casi el total del borde de la pantalla.

![](img/mejoras.jpg "Mejoras aplicadas al videojuego")



<br />


## Dudas en YouTube

En esta lección vamos a responder a una duda muy común que suele aparecer en este tipo de videojuegos cuando se cambia un objeto de dirección durante el transcurso del videojuego. Esta duda la plantea Jordi a través de un comentario en nuestro canal de YouTube.

![](img/duda-de-jordi.jpg "Duda de Jordi")

**Problema**

Cuando el objeto Bola toca al objeto Player 1 o Player 2, realizamos el cambio de dirección mediante la ecuación matemática (dirección * -1) y además le añadimos una pequeña desviación de 5º. El problema es que según varios factores (tamaño de la bola, velocidad de nuestro ordenador, etc.) se realizan varios cambios de dirección, sin que la bola llegue a desplazarse, lo que crea el efecto de que la bola queda enganchada a la paleta como comenta Jordi en el comentario.

**Solución**

Para solucionarlo basta con añadir un bloque para que la bola se desplace obligatoriamente justo después de cambiar de dirección, y de esa forma, evitar que vuelva a tocar la paleta en el mismo instante.

![](img/duda-de-jordi-solucion.jpg "Duda resuelta")



<br />



## Retos de Scratch

Si ya has completado todas las lecciones del tutorial te proponemos resolver los siguientes retos de programación con Scratch.

### Reto 1: El primero en llegar a 10 puntos gana

Si juegas durante mucho tiempo te derás cuenta que el videojuego no termina nunca. En este reto te propongo añadir a la programación una condición que muestre un mensaje por pantalla cuando un jugador llegue a 10 puntos. Esta programación deberás realizarla en el escenario.

![](img/reto-1.jpg "El primero en llegar a 10 puntos gana")
