# Curso de Diseño Web con CSS Grid y Flex-box

[Project Figma](https://www.figma.com/file/hRGY414K81hDUUWFrbGyP4/Neumorphism?type=design&mode=design&t=8t4S9x7mmpc2Con7-1)

## Flujo normal del documento: Display block, inline e inline-block

El flujo normal del documento sera la forma en que se mostraran los elementos si no modificamos nada, se basan en block e inline ambas propiedades se usan a lo largo del desarrollo como cuando usamos display: grid; o display: inline-grid; estarás marcando de alguna forma si el comportamiento externo es de bloque o en línea además que en la segunda propiedad indicas que comportamiento interno tendrá.

- **Display**:Definir el tipo de visualización de un elemento.
- Cuando usamos **display: flex;** o **display: grid;** Nos centramos más en los valores y no en la propiedad por si sola.

### Block and Inline elements

- **Block**: Se extienden ocupando todo el espacio disponible para ellos.
- **Inline**:
  - Son como palabras en una oración, una después de otra.
  - Se separan por medio de un espacio en blanco entre ellos.

El comportamiento de los elementos en bloque y en línea es fundamental para CSS y el hecho de que un documento HTML marcado correctamente será legible por defecto. Este diseño se conoce como "Diseño de bloque y en línea" o "Flujo normal" porque esta es la forma en que los elementos se presentan si no les hacemos nada más.

### Inner y Outer

- Block e Inline definen:

  - Valor externo de visualización.
  - Valor interno de visualización.

- Lo que significa es que cuando usamos **display: grid;** estamos diciendo **display: block-grid**;

- Un elemento que tenga los atributos de bloque puede establecer:

  - Ancho
  - Alto
  - Padding
  - Margin
  - Estirarse en todo el espacio

- Esta forma de pensar es util porque cuando usamos **display: inline-flex;**

  - Pensaremos que el primer valor es el comportamiento externo y el segundo valor es el interno del contenedor.

- Siempre volveremos al **flujo normal del documento**
  - Si trabajamos de esta forma obtendremos:
    - Flujo más agradable y legible.
    - CSS mucho más fácil.
    - Menos probable de tener problemas de accesibilidad (ya que está trabajando con el orden de los documentos que es exactamente lo que está haciendo un lector de pantalla o una persona que revisa el documento).

## Contextos de formato: Formato de Contexto de Bloque (BFC)

Es el layout interno de un elemento, que se comporta de manera independiente a como se comporta el resto de la página

Si bien maneja la estructura interna de un elemento, utilizando position se puede sacar al elemento del flujo normal del documento, haciendo que este se reordene de una forma distinta

### ¿Que pasa con flex-box y grid?

Ambos formatos nacieron con la intensión de facilitar el diseño de la página. Mientras flex-box se basa en un formato donde se le da flexibilidad a los elementos y al contenedor, grid adquiere un formato de cuadricula realmente fácil de ordenar.

### Inline-block

Inline-block es bastante fácil de entender. Consta en una fusión de ambas partes, donde al igual que inline-flex e inline-block, externamente el elemento se sitúa de forma inline, pero por dentro puede adoptar propiedades block como width, left, etc..

### flow-root

La propiedad flow-root en CSS se utiliza para crear un contexto de formato de bloque y establecer un nuevo contexto de formato de bloque para sus contenidos. Esto ayuda a limpiar el flujo del documento y solucionar problemas relacionados con elementos flotantes dentro de un contenedor. Es similar a utilizar clear-fix para limpiar el flujo del documento, pero de una manera más sencilla y elegante. El elemento al que se aplica la propiedad flow-root sigue siendo de bloque.

## Posicionamiento

El contexto de apilamiento es la conceptualization tridimensional de los elementos HTML a lo largo de un eje-Z imaginario relativo al usuario que se asume está de cara al viewport o página web. Los elementos HTML ocupan este espacio por orden de prioridad basado en sus atributos.

Cuando trabajamos con la web, es esencial tener en cuenta tres ejes: los ejes X y Y, que representan la posición horizontal y vertical de los elementos, y el eje Z imaginario, que va desde la pantalla hasta la vista del usuario.

En este contexto, las cajas juegan un papel crucial, ya que se sobreponen unas sobre otras. Un ejemplo común es un modal que se coloca encima de todo el sitio web. El concepto de apilamiento se asemeja a una pila, donde las cajas se ubican en orden de prioridad. Es importante destacar que nem todos los elementos pueden crear este efecto de apilamiento.

Un contexto de apilamiento es formado, en cualquier lugar del documento, por cualquier elemento que:

- Sea el elemento raíz (HTML).
- Tenga posición (absoluta o relativa) con un valor z-index distinto de auto.
- Position: fixed.
- Un elemento flex con un valor z-index distinto de auto, que sera el elemento padre display: flex/inline-flex.
- Sean elementos con un valor opacity menor de 1.
- Elementos con un valor transform distinto de none.
- Elementos con un valor mix-blend-mode distinto de normal.
- Elementos con un valor filter distinto de none.
- Elementos con un valor perspective distinto de none.
- Elementos con un valor isolation igual a isolate.
- Especifican cualquier atributo superior en will-change incluso si no especificas valores para estos atributos directamente.
- Elementos con un valor -webkit-overflow-scrolling igual a touch.

## Diferencias entre flex-box y CSS grid

### Flex-box

Nos ayuda a distribuir los elementos y alinearlos, es **unidireccional**, eso quiere decir que solo va en un a dirección, va vertical o va en horizontal.

Las propiedades que tiene un contenedor padre en flex-box son:

- display.
- flex-direction.
- flex-wrap.
- flex-flow.
- justify-content.
- align-items.
- align-content.

Las propiedades de elementos hijos son:

- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self

### Grid

Nos permite alinear elementos en filas y columnas, es bidemensional, podemos alinear elementos en dos direcciones.

Las propiedades de contenedores padre son:

- display.
- grid-template.
- gap.
- justify-items.
- align-items.
- justify-content.
- align-content.

Propiedades de elementos hijo:

- grid-column.
- grid-row.
- grid-area.
- justify-self.
- align-self.

![image](https://miro.medium.com/max/880/1*L-udJojk8cUUCXMyKB1IKQ.png)
![image](https://miro.medium.com/max/2708/1*htfdNmRIIFu_veRaFOj5qA.gif)
![image](https://cdn-media-1.freecodecamp.org/images/HbnMZT330ylw5idocqrjOfp9DrlZt9JrJm9o)
![image](https://cdn-media-1.freecodecamp.org/images/u9tCV-zRt3qpgSyNQt53e-eRz0-HIrsqqOk-)
![image](https://miro.medium.com/max/2562/1*6NUIFlnX9SAanhWeOwt3Bg.gif)

## Similitudes entre Flex-box y CSS Grid

Flex-box y CSS Grid comparten dos similitudes clave: las relaciones entre padres e hijos inmediatos y los ejes de alineamiento.

En cuanto a las relaciones, tanto los padres tienen hijos como los hijos pueden ser padres, siempre y cuando se defina correctamente qué contenedores desempeñarán esos roles. Esta claridad en la jerarquía facilita la aplicación de las técnicas adecuadas.

En relación a los ejes de alineamiento, CSS siempre trabaja con dos ejes: el inline axis (eje de fila) y el block axis (eje de columna). Para estos ejes, tenemos propiedades como Justify, que afecta al inline axis, y Align, que afecta al block axis. Ambas propiedades tienen puntos de inicio (start) y puntos finales (end), siendo el predeterminado de izquierda a derecha para el inline axis y de arriba a abajo para el block axis. Estos conceptos son fundamentales para comprender y aplicar de manera efectiva Flex-box y CSS Grid.

## ¿Qué son los Modern CSS Layouts?

Es interesante observar la evolución del diseño CSS a lo largo del tiempo. En 1996, se ideó un modelo de diseño "basado en marcos", que luego evolucionó con el lanzamiento del "Advanced Layout Module" en 2005. Este módulo posteriormente se transformó en el "Template Layout Module" en 2016.

A lo largo de estas transformaciones, la búsqueda de tener control sobre columnas, filas, tipografías y una organización eficiente del contenido, incluyendo elementos como encabezados y pies de página, ha sido constante. El layout CSS ha experimentado cambios drásticos, redefiniendo la manera en que desarrollamos la interfaz de nuestros sitios.

En la actualidad, contamos con diversas opciones y enfoques reales en términos de métodos de diseño en CSS. Como desarrolladores, es crucial mantenernos actualizados con la comprensión actual del layout, ya que nos enfrentamos a decisiones sobre qué enfoque adoptar al construir nuestros sitios. Exploraremos diferentes layouts y las diversas formas de construirlos para adaptarnos a las demandas cambiantes del diseño web.

Cuando hablamos de "Modern CSS Layouts", nos referimos a un concepto que tiene más de 10 años. En el contexto de la web en 2010, algunas de las características clave incluían:

- Progresivamente mejorado.
- Adaptable a diversos usuarios.
- Modulares y eficientes.
- Tipográficamente ricos.

### Progresivamente mejorado

- Base sólida e ir añadiendo estilos complejos para aquellos navegadores que pudieran soportarlo.
- En ese momento la compatibilidad entre navegadores era notorio.

### Adaptable a diversos usuarios

- Al tener una gran cantidad:
  - La amplia gama de navegadores.
  - Dispositivos.
  - Resoluciones de pantalla.
  - Tamaños de fuente.
  - Tecnologías de asistencia.

### Modulares y eficiente

- El CSS se pueda dividir en fragmentos que funcionan de forma independiente para crear componentes de diseño que se pueden reutilizar de forma independiente.
- Se hablaba de un framework que permitiera a los desarrolladores escribir código frontend modular rápido, fácil de mantener y basado en estándares.

## Design System y detalles visuales a tener en cuenta

El concepto de Design System es intrigante y esencial en el diseño de productos digitales. Se trata de una colección de componentes reutilizables respaldados por estándares claros, actuando como un plan maestro que se convierte en la fuente de la verdad. Este enfoque sirve como referencia para garantizar que todos los involucrados en el desarrollo del producto estén alineados.

Empresas líderes como Airbnb, Uber e IBM han transformado la manera en que diseñan productos digitales al implementar sus propios sistemas de diseño exclusivos. La consistencia es clave, y estas empresas han logrado cambiar el ritmo de creación e innovación en sus equipos mediante el uso de una colección de componentes repetibles y estándares que guían su aplicación.

La creación de un Design System involucra a todo el equipo de producto, desde programadores y diseñadores hasta gerentes y el equipo C-suite. El proceso comienza con un inventario que abarca colores, logotipos, encabezados, pies de página, formularios, código, entre otros. A través del consenso, se establecen pautas para el diseño, la codificación, la presentación y la comunicación.

Las decisiones tomadas por el equipo impactan directamente en el código y se basan en las necesidades del producto. Estas decisiones generan herramientas y procesos que mejoran la eficiencia y la coherencia del desarrollo.

Para revisar estos temas, se pueden explorar guías de diseño, como la de Shopify Polaris, que ofrecen orientación valiosa. Además, el uso de frameworks CSS como Tailwind CSS facilita la implementación de ciertos aspectos como espaciados y breakpoints. Estas herramientas son fundamentales para la creación y mantenimiento exitosos de Design Systems.

## Tendencias de diseño UI/UX: Fase de inspiración y creatividad

- **Jerarquia**, tener unos elementos mas grandes que otros, basados en la relevancia e importancias que le queremos dar a cada uno de ellos.

- **Contraste**, ejemplo el botón nos indica que nos están ayudando para poder presionarlo y ya con eso podemos jugar con el tema de contraste y de colores y ayudar también al usuario a leer sin leer prácticamente.

- **Proximidad**, que ver con el tema de consistencia por ejemplo vemos items en nuestras app que tienen mucha semejanza ya sea en colores, iconos y demás, ya sabemos que tiene que ver con una sección o una parte que es del mismo grupo etc.

- **Balance**, El tema de contraste y de colores, también puede jugar un papel bastante importante cuando queremos hablar de importancia o relevancia de un contenido en especifico.

_Podemos buscar también inspiración para poder realizar nuestros proyectos, uno de ellos es The state of UX in 2021, 100 lecciones bastante útiles a nivel de todo._

- **Ilustraciones animadas**, Es muy importante tener en cuenta el tema de rendimiento y de performance.

- **Garantizar**, también garantizar a las personas que independientemente que tengan datos o no puedan ver nuestros sitios,

- **Micro intercesiones**, normalmente no son animaciones, pero es lo que le indica al usuario que si esta haciendo clic o tag en algún lado, esos pequeños detalles en la web nos indican ciertas cosas y con eso le damos un gran peso a nuestra pagina, los pequeños detalles también son importantes.

- **UI**, Es tema mas que todo visual de colores y demás.

- **UX**, es la experiencia o emociones que transmite el proyecto (sistema, app, etc).

- **Realidad Virtual**, normalmente existen app que pueden decirnos como ver ciertos sitios, que si te pones tus gafas vas a ver de esta forma y de esta otra, ejemplo de que si tienes que hacer un tour virtual de de una casa o algún carro, etc.

- **Realidad aumentada**, supongamos que queremos comprar una planta, y esa planta la sumergimos en el lugar donde quisiéramos colocarla ya sea dentro de una casa, inmediatamente vamos la poder ver en el sitio que la necesitemos, todo depende el, juega un papel super interesante

- **Neo morfismo**, juega mucho con las sombras y también esta relacionado con otras tendencias como lo es material design y flat design que ya todo depende de la dirección de la luz.

- **Asymmetrical layouts**, es poder jugar con layouts asimétricos, en este caso tenemos imágenes que pueden ser muy sutil, que se vean también muy elegantes pero que sean distribuidas en diferentes partes.

### Finalize este curso en 6h
