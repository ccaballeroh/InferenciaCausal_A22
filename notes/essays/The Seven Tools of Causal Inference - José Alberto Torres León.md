
# The seven tools of causal inference

### Judea Pearl presenta en su artículo "The Seven Tools of Causal Inference, with Reflections on Machine Learning" las bondades de los Modelos Causales Estructurales (Structural Causal Models - SCM). En este escrito hago un reporte del contenido de dicho artículo desde mi punto punto de vista.

En primer lugar, Judea presenta tres obstáculos de enfrenta el Machine Learning (ML) y que impiden que cumpla la expectativa de mostrar o contar con inteligencia "a nivel humano".

El primero de ellos, es la poca capacidad de adaptación, esto es, que los sistemas de ML reaccionen de manera satisfactoria a condiciones diferentes a las que han sido programados (o entrenados) para resolver. 

También, otro de los obstáculos de los algoritmos de Machine Learning es que la gran mayoría de ellos son "cajas negras", es decir, artefactos a los que les proporcionamos una entrada, llevan a cabo algún procesamiento sobre ella, del cual desconocemos los detalles, y finalmente entregan una salida como resultado de su ejecución.

El tercer obstáculo que menciona es la falta de entendimiento de conexiones de causa-efecto. Este último resulta, para Judea Pearl, necesario para el desarrollo de sistemas de inteligencia artificial que realmente cuenten con "inteligencia a nivel humano". Este entendimiento de conexiones causa-efecto debería dotar a la computadora de mecanismo para crear una representación de su ambiente, interrogarla y proponer cambios, teóricos o hipotéticos, permitiendole "imaginar" cambios en el ambiente.  
 
Sobre estos obstáculos hay algunos puntos que me gustaría comentar. Para la capacidad de adaptación a condiciones distintas al entrenamiento, sí existen esfuerzos por lograr que los sistemas de ML puedan resolver problemas distintos a los de su entrenamiento, tenemos el caso de los agentes inteligentes entrenados en XLand [1], que logran resolver problemas que nunca enfrentaron durante el entrenamiento. Hago esta mención, para distinguir que algunos obstáculos y faltas de capacidades mencionadas por Judea Pearl en su artículo más que ser del Machine Learning en general, son propias del aprendizaje supervisado y no supervisado, sin embargo, el aprendizaje por refuerzo, que es considerado un tipo de ML, no tiene las mismas limitantes que los otros dos tipos de aprendizaje mencionados, por lo tanto, no coincido en que generalice de esa manera.

Por otro lado, aunque para muchos de los usuarios de estos algoritmos pudiera no ser de gran importancia comprender lo que pasa dentro de la caja negra, personalmente coincido con Pearl en que es necesario contar con algoritmos más del tipo de caja blanca o caja transparente, donde son conocidos todos los detalles del procesamiento que se hace para obtener una salida. Contar con cajas blancas y transparentes es lo ideal, pues permite un mejor desarrollo y manetenimiento de los sistemas ya que, en caso de fallos, entre más cajas negras tenga un sistema es más díficil saber qué parte de él falló y cómo podría arreglarse.

En cuanto al tercer obstáculo, sí, creo que el entendimiento de las conexiones causa-efecto le daría a las inteligencias artificiales una mayor capacidad de resolución de problemas, me cuestiono si realmente lo que buscamos al desarrollar inteligencia artificial es una inteligencia a nivel humano y a qué se refiere realmente con "inteligencia a nivel humano".

Continuando con el artículo, luego de exponer los obstáculos, se mencionan los tres niveles de la jerarquía causal, enumerados de la siguiente manera:
    1. Asociación - Involucra relaciones estadísticas obtenidas de los datos en bruto
    2. Intervención - Involucra hacer modifiaciones al mundo observado y evaluar el resulado obtenido de ellas
    3. Contrafactual - Involucra plantear escenarios imaginarios sobre el mundo real, requiriendo de razonamiento retrospectivo.
    
Cada nivel de la jerarquía se asocia con un tipo de algoritmo. Aunque, coincido con el autor en casi todo, no considero adecuado incluir todo el ML como parte del nivel de **asociación**, ya que, nuevamente, el aprendizaje reforzado debería de estar incluido como parte del nivel **intervención**, pues la premisa de este tipo de aprendizaje es generar los datos de entrenamiento a partir de la interacción con el ambiente, lo cual creo yo, colocaría este tipo de ML dentro del nivel 2 de la jerarquía.

Finalmente, menciona que para las preguntas en el nivel **contrafactual** de la jerarquía causal, sólo los modelos basados en relaciones funcionales o estructurales pueden computar sus respuestas. Como parte de esos modelos, presenta los "Modelos estrcuturales causales", que constan de tres partes: modelos gráficos, ecuaciones estructurales y lógicas contrafactual e intervencional.

Para dar respuesta a las preguntas contrafactuales, estos modelos cuentan con 7 herramientas, que son:
1. Codificación de suposiciones causales, darle conocimiento al sistema.
2. Do-calculos, predicción del efecto de intervenir.
3. La algoritmización de contrafactuales, uso de ecuaciones estructurales.
4. Análisis de mediación y la evaluación de efectos directos e indirectos.
5. Adaptabilidad, válidez externa y sesgo de selección de muestra. 
6. Recuperación de problemas por información faltante.
7. Descubrimiento causal, inferir modelos compatibles con los datos.

En conjunto, estas herramientas pueden obtenerse a partir del modelo de SCM presentado, dando solución a las preguntas del tercer nivel de la jerarquía causal. En otras palabras, dotando a las IAs de la capacidad de razonamiento retrospectivo, o al menos, un modelo de él.

Finalmente, presenta las conclusiones y presenta una idea en sus últimas líneas que me gustaría retomar y es la visión de que una simbiosis entre los métodos de machine learning y de inferencia causal podría ser el paradigma dominante de la siguiente generación de IA, en lo cual estoy completamente de acuerdo. Creo que cada enfoque y tipo de algoritmo puede enriquecerse del resto, esto lo comprobé en el campo de la Generación Procedimental de Contenido, disciplina en la que la hibridzación de algoritmos (de búsqueda y optimización, de ML, basados en reglas, etc.) es cada vez más común y ha demostrado dar mejores resultados que cada enfoque por separado. Por lo tanto, considero que en poco tiempo leeremos acerca de estos híbridos de ML e inferencia causal.


[1] Team, O.L., Stooke, A., Mahajan, A., Barros, C., Deck, C., Bauer, J., Sygnowski, J., Trebacz, M., Jaderberg, M., Mathieu, M., McAleese, N., Bradley-Schmieg, N., Wong, N., Porcel, N., Raileanu, R., Hughes-Fitt, S., Dalibard, V., & Czarnecki, W.M. (2021). Open-Ended Learning Leads to Generally Capable Agents. ArXiv, abs/2107.12808.


```python

```
