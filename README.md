### ## ## ¿QUÉ ES UNA ANIMACIÓN? 🎭
Una animación podría ser descrita como un conjunto de fotogramas que cuenten con un estado inicial y final, compuesto de distintos puntos medios que conforman la misma. Además, desde pequeños nuestros ojos 👀 han sido entrenados de forma involuntario al momento de ver las caricaturas a través del televisor.

### ## ## Principios de animación para la web 💻
Actualmente, en el desarrollo web, podemos contar con diversas animaciones realizadas en su mayoría con CSS. Para ello, existen principios a seguir, que se crearon con el fin de optimizar y aprovechar al máximo esta función. Estos principios describen cómo se puede utilizar la animación para sumergir a los espectadores en un mundo creíble 👓. Un dato interesante, es que dichos principios fueron utilizados como metodología de trabajo para las animaciones que Disney diseñaba en aquellos tiempos.

**Entre ellos tenemos:**
Squash and stretch
Anticipation
Staging
Straight-Ahead Action and Pose-to-Pose
Follow Through and Overlapping Action
Slow In and Slow Out
Arc
Secondary Action
Timing
Exaggeration
Solid drawing
Appeal
Contribución cr

### **CLASE 1**

**Counter CSS**
counter-reset: Crea o reinicia un contador.
counter-increment: Incrementa un valor del contador. 
content: Inserta el contenido generado (debe usarse con un pseudoelemento). 
counter(): Función que agrega el valor de un contador a un elemento.

Para crear contadores en CSS:
ocupamos 3 propiedades:

counter-reset: La cual basicamente nos genera un contador. A esta propiedad le debemos dar el valor del nombre que le pondremos al contador:

```css
 body{
            counter-reset: game;
        }
```

Para aumentar el valor del contador, utilizamos counter-increment al cual le daremos como valor el nombre del contador a incrementar.

```css
   input:checked {
        counter-increment: game;
    }
```

Por ultimo, si deseamos desplegar el texto, podemos hacer uso de content el cual refiere al contenido que tendra el selector en el que esta siendo usado:

```css
.total::after {
    content: counter(game);
}
```

## **Clase 5**

Propiedades para la duración de la animación ⌚
En este artículo veremos dos propiedades, las cuales su definición es la siguiente:

Propiedad animation-duration ⌛
Nos indica cuanto durará nuestra animación, solo recibe un valor que sería el tiempo, puede estar en segundos, milisegundos, etc. Los cuales serían: :::(Info) animation-duration: time | initial | inherit; :::

Propiedad animation-iteration-count ⌛
Nos indica cuantas veces se repetirá nuestra animación, también recibe solo un valor, y pueden ser los siguientes: :::(Info) animation-timing-function: linear | ease | ease-in | ease-out | ease-in-out | step-start | step-end | steps(int, start | end) | cubicbezier(n, n, n, n) | initial | inherit; :::

## **Clase 6**

Propiedad animation-name 🤓
Animation puede tener solo un valor, o varios.

Con estas propiedades, le colocamos un nombre a la fracción de código que queremos animar, para que el keyframe sepa a quién debemos animar. ¿Keyframes?, este extraño nombre tiene una función indispensable en la creación de animaciones, así que veremos una breve definición a continuación 🤯.

Keyframes 🎯
Básicamente el uso de la directiva @keyframes te permite definir el comportamiento de tu animación punto por punto, y cualquier elemento puede usar esta animación por medio de la regla animation-name.

Dentro de @keyframes especificamos cada punto de nuestra animación por medio de porcentajes 💎. Podríamos tener un @keyframes de esta forma:

@keyframes jump {

    /* Punto A */
    0% {
    }

    /* Punto B */
    40% {
    }

    /* Punto C */
    60% {
    }

    /* Punto D */
    90% {
    }

}
Los porcentajes pueden ser los que tú quieras, pero lo más importante a tener en cuenta es que mientras más cerca esté un porcentaje de otro más rápido será la transición de un punto a otro 😄.

## **Clase 7**
Animation timing function ⌚
Básicamente es la aceleración con la cual correrá nuestra animación.

Animation delay ⏰
Es el tiempo que nuestra animación tardará en empezar.

Animation Iteration Count 📒
Es el número de veces que se repetirán nuestra animación.

## **Clase 8**
Propiedades 🎯
📍 Animation direction 📍 Animation fill mode 📍 Animation play state

Animation Direction 🗽
Dirección de la animación.

Normal: La animación se reproduce hacia delante en cada ciclo. Por defecto.
Reverse: La animación se reproduce hacia atrás en cada ciclo.
Alternate: La animación se invierte en cada ciclo, y la primera iteración se reproduce hacia adelante.
Alternate-reverse: La animación invierte la dirección en cada ciclo, y la primera iteración se reproduce hacia atrás.

Animation Fill Mode 📢
Estado de cierta animación. Al inicio o final.

Animation Play State ⏯
Define si la animación se reproduce o es pausada. (running or paused)

## **Clase 9**
Hablaremos de todo el trabajo de renderizado de la web. Que sería básicamente unos procesos, como lo vemos a continuación:

🐱‍🏍 JavaScript 🐱‍🏍Style 🐱‍🏍 Layout 🐱‍🏍 Paint 🐱‍🏍 Composite

El día de hoy, hablaremos de estas últimas tres, estos son los procesos que tienen que hacer algunas de nuestras propiedades para poder renderizarse en la web 💻. Sucede en cuestión de milisegundos.

Composite: Ordena las partes de la página. Propiedades como opacity y transform.
Paint: Rellena píxeles. Implica colores, imágenes, textos, sombras, etc.
Layout: Diseño de la página. Ancho, margin, padding, border, etc.
Si nos dirigimos a csstriggers.com{target="_blank"}, podremos ver todas las propiedades de CSS que utilizamos y cómo actúan en los diferentes navegadores y motores.

Existen algunas propiedades en css que hacen que las paginas tarden mas en cargar. Esto se debe a que tienen que pasar por ciertas “capas” de renderizado hasta que se pinten en la pantalla.

En pocas palabras, las propiedades que tengan relacion con una gran cantidad de pixeles nos van a afectar en el performance de la pagina web. Por eso el background afecta al desempeño de la pagina web ⌛.

## **Recomendaciones**

Teniendo en cuenta lo que vimos en la clase de CSS Triggers, te dejo aquí 5 buenas prácticas para optimizar tus animaciones web:

Usa dentro de lo posible propiedades que solo tengan que pasar por el proceso de Composite.
Si necesitas animar alguna propiedad que sea muy costosa (como width, height, left, entre otras), trata de encontrar otra propiedad que sea menos costosa con la que puedas lograr el mismo resultado (o al menos un resultado similar).
Evita animar muchas propiedades al mismo tiempo.
Si necesitas esconder elementos, normalmente se usan las propiedades opacity y visibility en vez de usar la propiedad display (ya que es una propiedad no animable: Propiedades que pueden ser animadas).
Evita hacer animaciones que ocurran al hacer scroll, ya que el evento que escucha el scroll se ejecuta una gran cantidad de veces. Mejor espera a llegar a cierto punto de la pantalla y ahí ejecutas la animación.
