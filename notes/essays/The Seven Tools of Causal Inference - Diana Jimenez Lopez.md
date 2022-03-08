# The Seven Tools of Causal Inference


El siguiente video es una invitación al artículo de Judea Pearl "The Seven Tools of Causal Inference with Reflections on Machine Learning" publicado en _Communications of the ACM_ en 2019.

<iframe src="https://player.vimeo.com/video/314324108?h=7f5496bfdd" width="640" height="360" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

<p><a href="https://vimeo.com/314324108">The Seven Tools of Causal Inference</a> from <a href="https://vimeo.com/user4730653">CACM</a> on <a href="https://vimeo.com">Vimeo</a>.</p>
La Inteligencia Artifical ha logrado resultados asombrosos, sin emabargo aún hay problemas de tipo "´básico" para la mente humana que la Inteligencia Artificial no logra dominar con el conocido Machine Learning, tales como :

Problemas:
1. Adaptación: Los modelos rara vez reaccionan bien ante un contexto diferente al que fueron entrenados.
2. Explicatividad: Los modelos no nos pueden dar una explicación del resultado (ejemplo: desición).
3. No hay entendimiento causa-efecto 
4. Imaginación what if : No existe modelo que pueda contestar a preguntas del tipo "what if"
5. Contrafactuales: Este tipo de preguntas no son solo de tipo imaginativas, si no también restrspectivas, por lo que tampoco hay modelo que nos pueda ayudar en este tipo de preguntas. 

Para el tipo de preguntas que pretendemos resolver, en el artículo se proponen 3 niveles, los cuales son: 
1. Asosiación: Observar. 
2. Intervención :Hacer,  intervenir.
3. Contrafactuales: Imaginar, retrospección. 

Siendo direccionales  ya que se pueden responder preguntas del tipo 1 con información de tipo 2 y del tipo 2 con información del tipo 3, pero no vice versa, el top es lo contrafactual y por tanto lo más poderoso.

La inferencia causal nos proporciona herramientas que pueden combatir los problemas antes mencionados, las herramientas que se mencionan son:

1. Codificación de suposicones causales ,Transparencia y y comprobabilidad : Esto nos permite saber si las suposiciones son plausibles y si son compatibles con los datos
2. Do calculus y el control de la confusión: Gracias a este se puede predecir la factibilidad de las intervenciones y se identifica si las predicciones no pueden determinarse con los supuestos dados. 
3. La algoritmización de los contrafactuales : Un algortimo puede determinar si la probabilidad del supuesto en cuestión es estimable.
4. Análisis de la mediación y la evaluación de los efectos directos e indirectos: Cambios causa efecto
5. Adaptabilidad, validez externa y sesgo de selección de la muestra : Identificar los mecanismos responsables de los cambios, lo que permite adaptarse, gracias a las relaciones causa-efecto.
6. Recuperación de datos faltantes: Se puede producir una estimación.
7. Descubrimiento causal: Inferir el conjunto de modelos que son compatibles con los datos, descrubirir causas.

Como podemos observar estas herramientas nos permiten solucionar los problemas antes mencionados, y al solucionar estos problemas se abren una infinidad de problemas "reales"
 y específicos que se pueden resolver haciendo uso de inferencia causal, solamente es poder adaptar el problema en cuestión a a alguna de las herramientas presentadas.

## Referencias

- Pearl, Judea. “The Seven Tools of Causal Inference, with Reflections on Machine Learning.” _Communications of the ACM_ 62, no. 3 (February 21, 2019): 54–60. [https://doi.org/10.1145/3241036](https://doi.org/10.1145/3241036).