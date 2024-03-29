﻿`links` son una categoría especial de agentes (como tortugas y parcelas) en NetLogo para representar conexiones entre tortugas. Un enlace en sí mismo es solo una conexión entre dos tortugas (distintas) con alguna información adjunta. Con solo esta sencilla herramienta de conexiones entre tortugas, podemos representar relaciones muy sofisticadas entre tortugas como árboles genealógicos, relaciones de "amigos" en las redes sociales (comúnmente conocidas como "gráficos sociales") o incluso mapas de calle para software de navegación como Google Maps o Waze.

Puedes crear nuevos vínculos entre tortugas usando las primitivas `create-link-with` y `create-links-with` . Observa que `create-link-with` crea solo un vínculo entre dos tortugas y requiere una tortuga específica, mientras que `create-links-with` crea múltiples tortugas a la vez y requiere un conjunto de agentes.



```
ask turtles [
	create-link with one-of other turtles
	create-links-with other turtles with [color = green]
]
```


Cosas a tener en cuenta cuando usas `links`:

* NetLogo tiene un *editor de formas de enlace* en el menú *Herramientas*. Puedes usar este editor para diseñar formas de enlace personalizadas, como líneas de puntos, múltiples líneas paralelas o líneas curvas.
* De la misma manera que puede referirse a todas las tortugas del mundo con la palabra clave `turtles`, puedes referir a todos los enlaces del mundo con los `links` palabras clave. Por ejemplo, puedes usar esta palabra clave para cambiar el color o el grosor de la representación visual de los enlaces, como `ask links [set color grey]`.
* Puedes crear características de enlace personalizadas usando la primitiva de `links-own` (similar a `turtles-own` `patches-own`). Por ejemplo, si estás creando un modelo de infraestructura de Internet rural, tus enlaces pueden tener una característica de *ancho de banda*: `links-own [ bandwidth ]`.
* Puedes crear razas de enlaces personalizados con la primitiva `undirected-link-breed`. Por ejemplo, si su modelo va a tener dos tipos de enlaces, como `cables` y `satellite-connection`, puedes crear razas separadas como la `undirected-link-breed [cables cable]` y `undirected-link-breed [satellite-connections satellite-connection]`.


En el ejemplo de modelo a continuación, tenemos una red de computadoras representada con un servidor en el centro y otras computadoras terminales dispuestas en un diseño circular. Cada computadora está conectada al servidor con un enlace de rayas grises que representa una conexión pasiva. En cada tic, nuestro servidor inicia una conexión activa a un terminal aleatorio. Representamos las conexiones activas con un enlace verde. También usamos dos formas de enlace diferentes para las conexiones activas: un enlace recto simple que indica una recuperación de información y una conexión curva de tres líneas que indica la descarga de un archivo.