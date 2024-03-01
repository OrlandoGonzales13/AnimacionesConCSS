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
