## Tarea 2.1 The limitations of opaque learning machines
**Daniel Silva Contreras**

Hoy en día se habla de _Big Data_ y _Data Science_ de forma bastante vaga y generalizando. Incluso colocando bajo la misma etiqueta herramientas o tecnologías que no tienen nada que ver. Sin embargo, a pesar de lo mucho que se adornen las palabras, seguimos hablando de conjuntos enormes de datos de los cuales la mayoría de las veces no sabemos nada y de las personas que tienen que obtener un _algo_ de ese conjunto de datos. Algunas veces tienen más idea que otras.

Y es que no es raro no tener idea de lo que se quiere lograr, porque se tiene la idea erronea de que un conjunto de datos muy grande siempre nos va a _hablar_ y a decirnos justo lo que necesitamos. 
Esto desde luego no es cierto, un conjunto pequeño de datos significativos o muestreados adecuadamente pueden decirnos mucho y un conjunto de millones de datos puede arrojarnos conclusiones como que el cielo es amarillo.

Este problema es resultado de suponer que tanto los datos (como estén) con técnicas que  harán un ajuste de una función desconocida, seguramente con más parámetros de los que se necesitan, siempre resultará bien. O peor aún, creer que el rsultado será el que queremos o imaginamos.

El texto aborda esa ceguera que nos provocamos al dejar de lado el análisis dialéctico del problema que nos interesa y dejar todo en manos de herramientas, técnicas y/o algoritmos. Esto es, en lugar de analizar el problema desde distintos puntos de vista y cuestionar sanamente cada paso, solo se ingresan los datos a una caja negra, cruzamos los dedos y observamos el resultado seguido de un porcentaje. A veces eso sale bien, a veces sale mal y otras tantas, no sabemos ni qué es lo que sale.

Lo anterior no significa que las técnicas sen inútiles u obsoletas. De ninguna manera. Sin embargo, sí puede ser un indicador de que nos estamos autovendiendo espejos.

Debemos tener claro que el analizar un conjunto de datos tiene sus limitaciones, en tanto que son solo observaciones, y que de una u otra manera el análisis se verá afectado por nuestro propio criterio al utilizar uno u otra herramienta. 

La reflexión sería que debemos tener claridad en el funcionamiento de las herramientas que utilicemos, sus limitaciones y como mejorarlas, si es el caso. Pero nunca confiar ciegamente en Tensorflow o herramientas similares solo porque da "excelentes resultados" con el mismo conjunto de datos seleccionados especifciamente (como MNIST que se usa para todo).

En conclusión, no es que una técnica sea mejor o peor. Si estamos concientes de cómo funciona, por qué funciona y como usarlo perfecto, de lo contrario es seguro que no es la técnica o herramienta que debamos usar. Pueden parecer cajas negras, pero lo importante es que no lo sean para quien lo desarrolla. El mago siempre conoce sus trucos.