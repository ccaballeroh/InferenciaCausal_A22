# Sobre "The Seven Tools of Causal Inference" de Pearl (2019a)
### _Fernando Aguilar Canto_

En dos artículos, Judea Pearl (2019a, 2019b) dibuja sus ideas principales sobre el progreso actual del Aprendizaje Automático o _Machine Learning_. En general, su postura filosófica tiene las siguientes implicaciones:

1. Es posible el razonamiento causal (_Problema de la Causalidad_).
2. El análisis de datos en sí no es suficiente para alcanzar el nivel del razonamiento causal (_Empirismo vs Innatismo_).
3. Como corrolario de 1. y 2., el enfoque predominante del Aprendizaje Automático, basado en datos, no puede alcanzar el razonamiento causal.

Asimismo, Pearl da cierta dirección por la cual es posible automatizar el razonamiento causal e incluir en los modernos sistemas de Inteligencia Artificial. Es necesario indicar que tal razonamiento causal es un requisito necesario (mas no suficiente) para dirigirse a niveles de razonamiento comparables con el producido por humanos. 

Este ensayo se estructura de la siguiente forma: primero discutiremos (muy brevemente) sobre el problema de la causalidad y cómo Pearl considera que no solamente es posible sino necesaria la automatización del razonamiento causal. Después trataremos el problema del empirismo contra innatismo, y de qué forma la postura de Pearl tiene ciertos tintes de innatismo, al menos en una forma contemporánea. Finalmente, reflexionaremos sobre las implicaciones que tienen estas discusiones en el marco de los avances de la Inteligencia Artificial.

## Problema de la causalidad

"Causa" y "efecto" son dos palabras comunes en nuestro lenguaje ordinario. Muchas ciencias, como la epidemiología, parecen necesitar fuertemente de dicho concepto para enumerar causas de las enfermedades y cómo prevenirlas. Sin embargo, como muchos términos comunes en filosofía, resulta extremadamente difícil de definir apropiadamente. Para algunos pensadores, este concepto es polémico. 

Margáin (1998: 56) incluso declara que "como la monarquía británica, la noción de causa ha sobrevivido gracias a la común y errónea creencia de que no es dañina". Este autor propone un ejemplo que ilustra cómo la noción común de causa puede ser en extremo complicada. Consideremos el siguiente enunciado: 

(1) "El resbalón que se dio el general Hernández el 24-VII-1968 _causó_ su muerte"

En efecto, si eliminamos el hecho _cayó(general Hernández, 24-VII-1968)_, entonces el efecto no podría haberse dado. Sin embargo, es de observarse que no todo aquel que se cae muere, sino que otros factores deben ser considerados, otras circunstancias como su peso pudieron haber jugado cierto rol en la consecuencia. Este ejemplo nos ilustra cómo los fenómenos en realidad parecen ser multifactoriales y ciertos hechos previos tienen mayor o menor contribución al efecto. 

Además de Hugo Margáin y con mayor reconocimiento internacional, el empirista David Hume es uno de los filósofos más asociados con el estudio crítico de la causalidad. Algunos lectores de Hume como Rodríguez Sánchez (2004), identifican que el filósofo escocés distingue, primeramente, a la causalidad como una "cuestión de hecho" (esto es, empírico), y no _a priori_. Asimismo, lo que se observa en los razonamientos causales muchas veces es una _contingüidad_ entre un hecho A y B, una asociación espacio-temporal entre dos fenómenos que aparece de forma constante, pero no hay forma de probar que la conexión es necesaria. Por último, muchas veces dicho conocimiento causal es únicamente probabilístico, y no siempre tendremos una certidumbre total del conocimiento de los efectos.

Un ejemplo en el que se ilustra que la contigüidad de dos fenómenos no implica su causalidad es el siguiente: supongamos que siempre que aparece un fenómeno A, surge un fenómeno B después de un lapso de 2 segundos. Entonces podemos pensar que A causa B (A –> B). Sin embargo, puede ocurrir que exista un fenómeno C que cause A y B dos segundos después. Esta clase de problemas es parte del principio que afirma que _correlación no implica causalidad_. Sin embargo, como discutiremos, estos problemas tampoco implican que no dispongamos de ninguna forma de estudiar la causalidad, o entender cuándo un fenómeno no es causado por otro.

Para Pearl (2019a), la causalidad ha sido injustamente excluida de la modelación matemática durante mucho tiempo, lo cual representa un problema, ya que numerosas frases cotidianas no pueden representarse simbólicamente a pesar de ser evidentes. Por ejemplo, sabemos que la frase "El barro no causa la lluvia" es falsa, pero hasta recientemente no disponíamos de una forma matemática de representar ese aspecto de la realidad. De este modo, Pearl indica que las herramientas matemáticas ya existen, pero también que el razonamiento humano es capaz de entender bien a la causalidad, a pesar de los problemas filosóficos enfrentados.

Retomando el ejemplo (1), quizá de cierta forma la causalidad es un fenómeno markoviano: ciertos estados o circunstancias pueden llevarnos a otros estados con cierta probabilidad, así que ubicarnos en un estado (caerse pesando más de 40 kg) puede llevarnos a otro (morirse) con cierta probabilidad _p_. Por lo tanto, el estado i-1 del estado i (que puede ser multidimensional) es una _causa_ del estado i. Un enfoque markoviano moderno de la causalidad es tratado en Baier _et al_ (2021). Un importante antecedente de la Teoría Markoviana Causal es el Principio de la Causa Común de Reichenbach, que establece que si dos eventos A y B están positivamente correlacionados, entonces uno es causa del otro o tienen una causa común (Hitchcock y Rédei, 2020).


## Innatismo contra empirismo

El empirismo es la doctrina epistemológica que afirma la supremacía de la experiencia en las creencias justificadas, que usualmente se opone al innatismo, que afirma la existencia de conocimientos innatos (Audi, 2019). A pesar de que esta discusión tiene orígenes en el debate entre Aristóteles y Platón, es frecuentemente mencionado el empirismo inglés de John Locke y David Hume. En el caso del primero, concebía a la mente humana inicial como una tabla rasa (_tabula rasa_), a la cual se le agregaba información con la experiencia (Duschinsky, 2012). 

Nadie duda de que el conocimiento empírico juega un papel importante en las personas, pero ¿hasta qué punto existen estructuras o conocimientos innatos en las redes neuronales biológicas? Podríamos pensar que los pesos de las redes neuronales biológicas se ajustan mediante mecanismos de plasticidad, bien descritos por las reglas de Hebb (Dayan y Abbott, 2005), aunque queda la duda sobre si podrían existir cierto innatismo en algunos pesos. En el caso de la causalidad, se ha identificado que algunas reglas de aprendizaje hebbianas dependientes del tiempo, pueden formar la base del razonamiento causal (Bi y Poo, 1998; Masuda y Kori, 2007; Vogt y Hofmann, 2012). No obstante, dichas reglas no consideran los problemas sobre causalidad mencionados y sólo parecen ser detectores de correlaciones temporales. 

Por otro lado, parece ser claro que la arquitectura de las redes neuronas es innata, por lo que de manera inicial podemos considerar que los parámetros de nuestras redes son empíricos pero la estructura de la misma es innata. Esto último tiene importantes consecuencias filosóficas: ¿de qué forma la arquitectura de la red conserva cierto conocimiento? No obstante, sí se han encontrado pesos sinápticos "innatos" (Markram y Perin, 2011).

Pearl (2019a) establece que para alcanzar un completo razonamiento causal se requiere de la capacidad de construir modelos, generalmente representados en grafos, conformando las hipótesis (_assumptions_) del motor inferencial. Este modelo gráfico puede considerarse, en términos más epistemológicos, como una _teoría_. Teoría y datos son necesarios para responder preguntas. 

Los recientes avances en Neurociencia Computacional han permitido dilucidar que las redes neuronales biológicas también dependen de los modelos  (Wunderlich, Smittenaar y Dolan, 2012; Langdon, Sharpe, Schoenbaum, 2018), que corresponde a la discusión sobre los métodos _model-based_ contra los _model-free_. Si el cerebro opera de forma libre de modelos, entonces tenemos el caso más empirista: únicamente necesitamos datos. Pero la relevancia de la creación de modelos frente a los enfoques puramente basados en datos, nos muestran una visión menos empirista del cerebro y más a favor de los argumentos de Pearl (2019a). Esto no significa que los modelos en sí sean innatos, aunque quizá tengan cierta dependencia con la arquitectura neuronal. 


## Consecuencias sobre el Aprendizaje Automático

Frente a las propuestas descritas en Hassani, Huang y Ghodsi (2018), en donde se enumeran métodos diferentes de Big Data para el análisis causal, Pearl (2019a, 2019b) insiste sobre la imposibilidad de lograr conocimiento causal únicamente con datos. Dentro de la jerarquía de Pearl (2019a), los datos se encuentran en el nivel asociativo, por lo que los enfoques actuales (en el cual se incluye de forma mayoritaria el _Deep Learning_) no pueden superar este nivel. El siguiente nivel es el intervencional, que responde preguntas como "¿qué pasaría si hago X?" (que puede abordarse mediante el do-calculus), mientras que el último corresponde a los contrafactuales, respondiendo preguntas que no pueden corroborarse de forma exclusiva con datos como "¿por qué?", "¿qué hubiera pasado si ...?". 

Pearl también propone los Modelos Estructurales Causales (_Structural Causal Models_ o SCM), que consta de datos, un conjunto de hipótesis (modelos en grafos) y preguntas por responder, devolviendo como salida una fórmula para estimar la pregunta, una estimación de la respuesta y un índice de ajuste. Asimismo, proporciona siete herramientas para lograr la total automatización del razonamiento causal. En este sentido, Pearl no dicta la imposibilidad de tal hazaña, simplemente considera que la dirección que se está tomando no alcanzará nunca el nivel de razonamiento logrado por la humanidad.

Sin embargo, si bien estos pasos y consideraciones proporcionadas por Pearl, considero que los esfuerzos del _Deep Learning_ pueden ajustarse a estos requerimientos. Estas ideas, si bien señalan los límites de los enfoques contemporáneos en cuanto al rumbo a la Inteligencia Artificial General, indican qué pasos deben darse para tomar esta dirección. Autores como Possati (2021) están de acuerdo con este esquema y añaden otras consideraciones como la importancia de los sistemas emocionales en la toma de decisiones y cómo estos pueden codificarse en un sistema artificial. 

De acuerdo con el nivel intervencional, parece necesario que los sistemas con Inteligencia Artificial General tengan un "cuerpo", es decir, sean robots que se desplacen en el ambiente. En gran medida, considero que cuando Pearl habla de Aprendizaje Automático obvia por completo al Aprendizaje por Refuerzo, que de alguna manera realiza intervenciones y se ajusta al ambiente. Intentos por unir el Aprendizaje por Refuerzo con la teoría de Pearl (en particular el do-calculus) se han realizado (véase Zhang y Bareinboim, 2017). En efecto, muchas ideas del Aprendizaje por Refuerzo pueden aplicarse a robots. Es necesario decir que en seres humanos existe aprendizaje intervencional que se realiza sin intervenir, como es el caso de las neuronas espejo, las cuales se activan al observarse la actividad de otra persona y pueden ser claves para aprendizajes motoros (Heyes, 2010).

En cuanto al último nivel (contrafactual), anteriormente vimos cómo los métodos basados en modelos (_model-based_) agregan de alguna manera la parte de las hipótesis que aparece en los SCMs. Llama la atención de que Pearl los representa como grafos, siendo las redes neuronales grafos también, no veo imposible dicha transición. Y considerando que existe el _Deep Reinforcement Learning_ (Henderson _et al_, 2017), considero que los dos niveles superiores de la jerarquía de Pearl serán, eventualmente, alcanzados por redes neuronales (profundas).

### Revisión de razonamiento causal en sistemas artificiales basados en datos

Hemos visto como los argumentos de Pearl indican que el razonamiento causal está completamente privado para los modernos sistemas de Inteligencia Artificial. Para corroborar este hecho, hemos puesto a GPT-3 con el motor text-davinci-001 (supuestamente el mejor en razonamientos causales) a responder las siguientes preguntas, muchas de las cuales relacionadas con el razonamiento causal.

![[Captura de Pantalla 2022-02-22 a la(s) 12.18.50.png]]

![[Captura de Pantalla 2022-02-22 a la(s) 12.19.45.png]]

![[Captura de Pantalla 2022-02-22 a la(s) 12.22.56.png]]

![[Captura de Pantalla 2022-02-22 a la(s) 12.24.53.png]]

Como podemos apreciar, en muchos casos es capaz de identificar la causa de un fenómeno, mientras que en otros es completamente incapaz. Es curioso observar que su problema es el razonamiento en general, ya que en una de las preguntas razona correctamente que el VIH es un virus y que causa SIDA, pero no puede concluir que un virus causa SIDA. Asimismo, es posible tomar la perspectiva de que lo que está sucediendo no es razonamiento causal, sino que simplemente está generando textos que partieron de razonamientos causales de personas, pero no propios.

## Conclusiones

En este ensayo revisamos algunos puntos que considero relevantes en cuando al razonamiento causal, las ideas de Judea Pearl y sobre su implementación en sistemas de _Machine Learning_. Pearl es muy claro en dar su postura sobre los enfoques actuales: no hay forma de alcanzar razonamiento causal por medio de los enfoques que sólo toman en cuenta a los datos. Corroboramos este punto utilizando uno de los agentes conversacionales más fuertes de la actualidad, GPT-3, el cual fue capaz de responder algunas preguntas causales pero no todas. 

Sin embargo, hemos defendido la tesis de que los enfoques de redes neuronales artificiales, posiblemente implementadas en robots, pueden alcanzar los niveles de razonamiento que Pearl aspira. Esto no desacredita el trabajo de Pearl o sus ideas, simplemente consideramos que tal proyecto es alcanzable con este enfoque. Este razonamiento es natural: si somos nosotros redes neuronales vivientes, entonces quizá el uso de redes artificiales pueda lograr el razonamiento causal que nosotros tenemos y con ello dar un paso más hacia la Inteligencia Artificial General, la cual no sabemos si es posible. 


## Referencias


- Audi, R. (2019). _The Cambridge Dictionary of Philosophy._ 3a edicción. Cambridge University Press, Nueva York. 
- Baier, C., Funke, F., Jantsch, S., Piribauer, J., & Ziemek, R. (2021, October). Probabilistic causes in Markov chains. In _International Symposium on Automated Technology for Verification and Analysis_ (pp. 205-221). Springer, Cham.
- Bi, G. Q., & Poo, M. M. (1998). Synaptic modifications in cultured hippocampal neurons: dependence on spike timing, synaptic strength, and postsynaptic cell type. _Journal of neuroscience_, _18_(24), 10464-10472.
- Dayan, P., & Abbott, L. F. (2005). _Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems_. MIT press.
- Duschinsky, R. (2012). Tabula rasa and human nature. _Philosophy_, _87_(4), 509-529.
- Hassani, H., Huang, X., & Ghodsi, M. (2018). Big data and causality. _Annals of Data Science_, _5_(2), 133-156.
- Henderson, P., Islam, R., Bachman, P., Pineau, J., Precup, D., & Meger, D. (2018, April). Deep reinforcement learning that matters. In _Proceedings of the AAAI conference on artificial intelligence_ (Vol. 32, No. 1).
- Heyes, C. (2010). Where do mirror neurons come from?. _Neuroscience & Biobehavioral Reviews_, _34_(4), 575-583.
- Hitchcock, C., & Rédei, M. (2020). Reichenbach’s Common Cause Principle.[https://plato.stanford.edu/entries/physics-Rpcc/]
- Langdon, A. J., Sharpe, M. J., Schoenbaum, G., & Niv, Y. (2018). Model-based predictions for dopamine. _Current opinion in neurobiology_, _49_, 1-7.
- Margán, H. (1998). _Racionalidad, lenguaje y filosofía_. UNAM-IIF, Fondo de Cultura Económica. México.
- Markram, H., & Perin, R. (2011). Innate neural assemblies for Lego memory. _Frontiers in neural circuits_, _5_, 6. 
- Masuda, N., & Kori, H. (2007). Formation of feedforward networks and frequency synchrony by spike-timing-dependent plasticity. _Journal of Computational Neuroscience_, _22_(3), 327-345.
- Pearl, Judea (February 21, 2019a). “The Seven Tools of Causal Inference, with Reflections on Machine Learning.” _Communications of the ACM_ 62, no. 3: 54–60. [https://doi.org/10.1145/3241036](https://doi.org/10.1145/3241036).
- Pearl, Judea (2019b). “[The Limitations of Opaque Learning Machines](https://ftp.cs.ucla.edu/pub/stat_ser/r489.pdf).” _Possible Minds: Twenty-Five Ways of Looking at AI_, 13–19.
- Rodríguez Sánchez, R. A.. (2004). Conocimiento y causalidad en el pensamiento de David Hume. _Pensamiento. Revista de Investigación e Información Filosófica_, _60_(226), 145-161.
- Vogt, S. M., & Hofmann, U. G. (2012). Neuromodulation of STDP through short-term changes in firing causality. _Cognitive neurodynamics_, _6_(4), 353-366.
- Zhang, J., & Bareinboim, E. (2017, May). Transfer learning in multi-armed bandit: a causal approach. In _Proceedings of the 16th Conference on Autonomous Agents and MultiAgent Systems_ (pp. 1778-1780).
- Wunderlich, K., Smittenaar, P., & Dolan, R. J. (2012). Dopamine enhances model-based over model-free choice behavior. _Neuron_, _75_(3), 418-424.