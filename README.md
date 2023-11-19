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

    NOTA: Como ya sabemos de otras prácticas, siempre que se utilizan variables debemos de inicializarlas a un valor por defecto. 
    En este caso, le asignamos el valor en la función "Inicializar".

![](img/pong4.gif "Bandera verde - añadir variable")

Como se puede observar, la velocidad de la bola será siempre la misma. Haremos que se vaya incrementando en niveles posteriores.

![](img/pong4.png)

![](img/pong5.png)

<br />


## Jugadores

En primer lugar, se inicializan las posiciones origen de cada "pala" de los jugadores, en su eje X (valor 227) e Y (valor 0) respectivamente.

![](img/ini_jugador1.png) 
![](img/ini_jugador2.png)

    OJO: la paleta del jugador de la izquierda tendrá un valor negativo y el de la derecha positivo!!

A continuación, pondremos bloques para que al recibir la llamada del evento "Comenzar juego" cambiemos las posiciones de la coordenada vertical para que la paleta suba o baje según la tecla presionada. *¡CUIDADO, no asignes las mismas teclas para controlar a los dos jugadores distintos!*

    *Para el jugador de la derecha, usa las teclas: flecha arriba y flecha abajo.
    *Para el jugador de la izquierda, elige libremente las teclas. Para este tutorial, pondremos: "q" (arriba) y "a" (abajo).

### Jugador 1
![](img/jug1.png)

### Jugador 2
![](img/jug2.png)

Por último, modificamos la programación de la pelota para que rebote no sólo cuando toca un borde, sino que además deberá rebotar si toca cualquiera de las palas de los jugadores. Para eso, multiplicaremos la dirección que tengamos en ese momento por (-1), ya que el rebote debe ser la dirección contraria.

![](img/pelota_jug.png)

<br />


## Puntos


## Incrementar velocidad



## Mejoras a realizar:

- Añadir música de fondo. Debe sonar durante todo el rato, hasta que un jugador pierda.
- Añadir efecto de sonido para cada GOL marcado.
- Cuando un jugador pierda la partida, debe sonar un efecto de sonido distinto.
- Crear / Modificar fondo GAME OVER a vuestro gusto.


