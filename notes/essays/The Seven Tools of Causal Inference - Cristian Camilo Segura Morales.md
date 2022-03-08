# 7 herramientas para la inferencia causal

## Por: Cristian Camilo Segura Morales

Como complemento al análisis en donde hablábamos en aspectos generales de la inferencia causal, en este segundo artículo se realiza un análisis técnico más a detalle de la arquitectura propuesta con la que debe contar un modelo de inferencia causal y además de siete herramientas técnicas en el marco de trabajo propuesto por el autor el cual se detallará más adelante.

Como se indicaba en el anterior ensayo, usualmente debido a las altas expectativas de los usuarios y la gran atención focalizada en los sistemas autónomos independientes usualmente genera choques con expectativas en otras áreas de aplicación como lo es la transferencia de lo aprendido, la adaptación del dominio, aprendizaje a largo plazo y la explicabilidad han llegado a convertirse en unos de los obstáculos en el aprendizaje. Es precisamente este el objetivo de los sistemas de inferencia causal los cuales pretenden establecer conexiones de tipo causa y efecto. El autor realiza la descripción de una arquitectura compuesta por tres niveles de la siguiente manera:

1. Asociación: Capa compuesta por las relaciones estadísticas entre los datos puros. verificando relaciones simples con los datos que se cuenta en un instante de tiempo.

2. Intervención. Realiza una modificación a la vista actual de los datos mediante cambios a uno o varios de ellos y la implicación que esto tiene sobre los demás datos del modelo.

3. Contrafáctico. Incluye lo que se denomina razonamiento en retrospectiva ya que implica analizar escenarios en los que se hubiera tomado un camino alternativo a la opción principal.

La jerarquía no es puesta en orden aleatorio, sino que para ir subiendo en cada uno de los niveles es necesario contar con el nivel inmediatamente anterior generado finalmente una interdependencia entre los tres. si se cuenta con un modelo que puede contestar preguntas del tercer nivel, es posible contestar preguntas de los otros dos inferiores, pero si el modelo desarrollado únicamente responde a preguntas del primer nivel, no es posible responder preguntas del nivel de asociación o del de intervención, por lo cual son incluyentes de manera descendente, pero excluyentes de manera ascendente. en conclusión: contar con el tercer nivel hace el modelo más poderoso.

En un modelo usual de clasificación de sentimientos por nombrar alguno, usualmente el sistema realiza el aprendizaje con base en una serie de afirmaciones y una etiqueta de clase indicando esa frase a qué sentimiento está asociado, una situación como "La persona está deprimida porque su relación sentimental terminó de manera abrupta" por lo que este clasificador podía ser categorizado únicamente como un sistema de nivel 1 de acuerdo con la jerarquía. Si quisiéramos llegar a un sistema de nivel dos podría realizarse la inclusión de preguntas como "¿Si la relación no hubiera terminado la clasificación del sentimiento habría sido diferente? Y ya para llegar al nivel de jerarquía 3 una posible pregunta en el modelo podría ser algo como: "¿la relación no habría terminado si una de las partes involucradas no sintiera celos?"

El desarrollo de modelos matemáticos nuevos ha permitido el manejo de preguntas de tipo causa y efecto permitiendo realizar la codificación de este tipo de razonamiento contrafáctico y poder realizar la estimación de respuestas a este tipo de preguntas. El modelo matemático propuesto por el autor lleva como nombre "Modelos Estructurales Causales" (o SCM por su nombre en inglés) y está dividido en tres secciones: modelos gráficos que representan lo que los agentes conocen de su entorno, lógica intervencionista que ayuda a articular lo que se desea conocer y las ecuaciones estructurales son las que unen los dos primeros elementos en un conjunto orquestado de manera correcta. Al resultado de aplicar la fórmula matemática para realizar este tipo de estimaciones es conocido como el Estimador (Es).

Finalmente, el autor brinda una serie de 7 herramientas para el marco de trabajo SCM y como cada una de ellas contribuye en el razonamiento automático.

1. Codificación de suposiciones causales: transparencia y comprobabilidad. La transparencia permite a los analistas de datos a diferenciar cuando las suposiciones codificadas son admisibles o si se requieren suposiciones adicionales. La comprobabilidad permite determinar si las suposiciones realizadas con compatibles con el conjunto de datos con el que se cuenta y en caso de que no, se identifica las que requieren ajustes.

2. "Do-Calculus" y control de confusión. La confusión o causas sin observar eran consideradas el mayor obstáculo al momento de diagramar inferencias causales; pero de manera gráfica se solucionó con un método denominado "backdoor" y para los modelos que no aplica este criterio se utiliza un motor denominado "Do-Calculus" que realiza predicciones del efecto de políticas de intervención.

3. La algoritmización de los contrafactuales. El análisis contrafáctico lidia con el comportamiento de individuos específicos con conjuntos diferentes de características; por lo que se debe formalizar este razonamiento con la representación gráfica del punto anterior para codificar este conocimiento así cada algoritmo permite determinar si la probabilidad de una afirmación puede ser obtenida experimentalmente, con la observación o una combinación de ambos.

4. Análisis de mediación y evaluación de efectos directos e indirectos. La mediación realiza la transmisión de cambios de una causa a los efectos que puede desencadenar. Esta identificación permite generar explicaciones mediante el análisis contrafactico.

5. Adaptabilidad, validez externa y sesgo de selección de la muestra.

6. Recuperación de datos faltantes. En todo sistema hay situaciones que no permiten la adquisición correcta de los datos requeridos para su funcionamiento por ello en el modelo causal se pueden formalizar procesos que lidien con la falta de información mediante relaciones que permitan recuperación de información faltante y poder así obtener un dato estimado consistente de la relación deseada.

7. Descubrimiento Causal. El criterio de separación-d permite realizar la identificación y numeración las implicaciones probables de cierto modelo causal. Esto abre una brecha de posibilidades de inferir con suposiciones moderadas conjuntos de modelos que sean compatibles con datos y representar conjuntos de manera compacta.

En conclusión, con este marco de trabajo propuesto se cuenta con un sistema detallado de pasos con el que los investigadores pueden realizar los diferentes trabajos de creación de sistemas causales de una manera guiada y que permita llevar a buen término la implementación de cada uno de ellos. Por mi parte personal es un poco complicado cambiar el chip y empezar a ver los modelos de aprendizaje automático de esta manera ya que usualmente nos encontramos arraigados únicamente a la parte estadística pero no a la parte causal la cual puede conllevar a una diferencia significativa en el sistema implementado.