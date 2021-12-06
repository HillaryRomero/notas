
# Adjusting Word Embeddings with Semantic Intensity Orders
## ¿Qué hace? 
El objetivo común de estos enfoques es acercar las palabras semánticamente cercanas y alejar las semánticamente distantes, manteniendo cada vector de palabras sin alejarse demasiado de la posición original.
## ¿Cómo lo hace? 
En este estudio, partimos de uno de los tres tipos de vectores de palabras disponibles como base para nuestros estudios: GloVe, CBOW y Paragram-SL999 (Wieting et al., 2015); ajustamos cada uno de estos conjuntos de vectores con una variedad de métodos contrastivos. Nuestro primer sistema contrastivo es una línea de base que utiliza sinónimos y antónimos ("syn&ant") siguiendo el enfoque de Mrkši'c et al. (2016), que ajusta vectores de palabras para que la suma de las tres funciones objetivo de funciones objetivo de margen máximo se minimice.

## ¿Con qué clase de palabratrabaja? 
*Trabajaron con palabras léxicas: sinónimos, antónimos, hiperónimos.*

# DecodingWord Embeddings with Brain-Based Semantic Features
## ¿Qué hace? 
Decodificamos el contenido de las word embeddings mapeándolas en vectores de características semánticas interpretables.
Hemos llevado a cabo el mapeo de incrustaciones continuas en rasgos semánticos discretos con un doble objetivo: (i) identificar qué rasgos semánticos están mejor codificados en las incrustaciones de palabras; y (ii) utilizar las representaciones de rasgos propuestas para explicar el rendimiento de las incrustaciones en tareas de sondeo semántico.
  
## ¿Cómo lo hace? 
En cuanto al primer objetivo, hemos probado el método de decodificación de incrustaciones en varios tipos de MDS estáticos y contextualizados. Todos los modelos logran altas correlaciones entre las palabras y los rasgos, y los MDS basados en la dependencia tienen una ligera ventaja sobre los demás, en consonancia con los hallazgos de Abnar et al. (2018).
 
En cuanto al segundo objetivo, hemos aplicado nuestras representaciones de rasgos descodificados a la metodología de la tarea de sondeo, muy popular, para conocer qué piezas de información semántica captan realmente los clasificadores de sondeo. Para nuestros experimentos, probamos las incrustaciones originales en tareas de sondeo diseñadas para apuntar a la valencia afectiva, la animacidad, la concreción y varias clases de verbos derivadas de VerbNet para los MDS no contextualizados, y la animacidad del objeto directo y las alternancias verbales causales/incoativas para las incrustaciones contextualizadas. Si un clasificador binario consigue identificar si una palabra pertenece a una clase semántica sobre la base de su incrustación, esto se suele considerar como una prueba indirecta de que la incrustación codifica la información semántica pertinente. 
 
En nuestro trabajo, en lugar de considerar las tareas de sondeo sólo como experimentos de "caja negra", utilizamos los vectores de características decodificados para inspeccionar las dimensiones semánticas aprendidas por los clasificadores. 

## ¿Con qué clase de palabratrabaja? 
*Trabajaron con palabras léxicas: adjetivos positivos y negativos, sustantivos concretos y asbtractos, animados e inanimados y verbos.*




# Improving Lexical Embeddings with Semantic Knowledge
## ¿Qué hace? 
El objetivo de nuestros experimentos es demostrar el valor del aprendizaje de incrustaciones semánticas con información de recursos semánticos. En cada escenario, compararemos la incrustación de base de word2vec entrenada con cbow contra RCM solo, el modelo conjunto y Joint -- RCM. Consideramos tres tareas de evaluación: el modelado del lenguaje, la medición de la similitud semántica y la predicción de los juicios humanos sobre la relación semántica.


## ¿Cómo lo hace? 

En todos nuestros experimentos, llevamos a cabo el desarrollo del modelo y ajustamos los parámetros del mismo (C, cbow, RCM, conjunto de datos PPDB, etc.) en los datos de desarrollo, y evaluamos el modelo de mejor rendimiento en los datos de prueba. ¡Los modelos se denominan de la siguiente manera: word2vec para el objetivo de referencia (cbow o skip-gram), RCM-r/p y Joint-r/p para inicializaciones aleatorias y preentrenadas de los objetivos RCM y Joint, y Join RCMt!
para el preentrenamiento de RCM con incrustaciones conjuntas. A menos que se indique lo contrario, entrenamos utilizando PPDB XXL.
Inicialmente creamos datos de entrenamiento de WordNet, pero nos pareció que eran demasiado pequeños para afectar a los resultados. Por lo tanto, sólo incluimos los resultados de RCM entrenados en PPDB, pero mostramos las evaluaciones tanto en PPDB como en WordNet.
Entrenamos incrustaciones de 200 dimensiones y utilizamos incrustaciones de salida para medir la similitud. Durante el entrenamiento de los objetivos de cbow eliminamos todas las palabras con frecuencias inferiores a 5, que es la configuración por defectos de word2vec.

## ¿Con qué clase de palabratrabaja? 
*Trabajan con palabras léxicamente plenas*

# Learning Semantic Hierarchies via Word Embeddings

## ¿Qué hace?
El objetivo es entrenamiento de la incrustación de palabras, el aprendizaje de la proyección y la identificación de la relación entre hiperónimos.
identificación de la relación hipónima. 



## ¿Cómo lo hace? 
Dada una lista de hiperónimos de una entidad, nuestro objetivo es construir una jerarquía semántica sobre ella (Figura 1). Representamos la jerarquía como un grafo dirigido G, en el que los nodos denotan las palabras y las aristas las relaciones hipernímicas-hipónimas. Las relaciones hiperónimo-hipónimo son asimétricas y transitivas cuando las palabras no son ambiguas:
Aquí, L denota la lista de hiperónimos. x, y y z, denotan los hiperónimos en L.
En este documento utilizamos H para representar una relación hipernimia-hipónimo documento. En realidad, x, y y z son inequívocos como hiperónimos de una entidad determinada. Por lo tanto, G debe ser un grafo acíclico dirigido (DAG).

Este artículo propone un método novedoso para la construcción de jerarquías semánticas basado en la incrustación de palabras, que se entrena utilizando un corpus a gran escala. A partir de las incrustaciones de palabras, aprendemos la relación hipernimia-hipónimo mediante la estimación de
matrices de proyección que asignan las palabras a sus hipérnimos.Se introducen nuevas mejoras mediante un enfoque basado en clústeres para modelar las relaciones más precisas. A continuación, proponemos unos criterios sencillos para identificar si un nuevo par de palabras es una relación hipernímico-hipónima. A partir de las relaciones hipernímicas-hipónimas por pares, construimos automáticamente jerarquías semánticas.
En nuestros experimentos, el método propuesto supera significativamente a los métodos más avanzados y alcanza la mejor puntuación F1 del 73,74% en un conjunto de datos de prueba etiquetados manualmente.
etiquetado manualmente. Otros experimentos muestran que nuestro método es complementario a los anteriores métodos de extensión de jerarquías construidas manualmente. 


## ¿Con qué clase de palabratrabaja? 
*Trabajan con palabras léxicamente plenas*


# Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking
## ¿Qué hace? 
Emparejamiento semántico para determinar la similtud entre textos. 
En este artículo, no sólo implementamos varios modelos semánticos profundos, sino que también
proponemos una nueva arquitectura para resolver este problema, denominada modelo DMPSM. En detalle, nuestro modelo obtiene información de multipercepción, el significado semántico de toda la frase y la característica de interacción de las palabras, lo que ayuda a conseguir la mejor puntuación.
## ¿Cómo lo hace? 
Debido al limitado número de presentaciones, sólo presentamos y guardamos algunos modelos profundos con mejores resultados. Otros modelos sencillos con características sintéticas, como Logistic Re gresión logística, Random Forest, XGBoost, LightGBM y también el modelo profundo InferSent se utilizan en el apilamiento para obtener un mejor rendimiento. La Tabla 1 ilustra los resultados de los diferentes ap de los diferentes enfoques. El análisis se centra en dos perspectivas y nos ayudará a encontrar la mejor arquitectura de modelo único.
arquitectura de modelo único.

*¿Qué tipo de modelo puede obtener mejor el significado semántico de la secuencia de palabras?
de las palabras?*
La CNN puede capturar convenientemente la característica de N-gramas mediante núcleos de tamaño múltiple que
que ayudarán a emparejar la frase en diferentes granularidades. Observa una frase desde un punto de vista vi sual de vista, e ignora la relación secuencial de las palabras hasta cierto punto. En Por el contrario, el LSTM se utiliza a menudo para el modelo de lenguaje, y es bueno para modelar la formación de secuencias. secuencia.
Podemos encontrar que MPCNN obtiene una puntuación más baja que Bi-MPM Bi-LSTM o SSE,
y como lan et al[2] indica que la codificación de la información de contexto secuencial con LSTM es crítico.

*¿Qué tipo de modelo es mejor, el de codificación de frases o el de interacción?*
La puntuación del modelo SSE es ligeramente inferior a la de Bi-MPM, y puede verse en el análisis de lan et al[2] que el modelo interactivo es generalmente mejor que el modelo basado en la codificación.
Sin embargo, podemos ignorar cuál es mejor. Estos dos tipos de modelos resuelven los problemas desde diferentes ángulos, combinamos las dos ideas y proponemos el modelo DMPSM.
Para obtener un mejor rendimiento, realizamos un apilamiento de estos modelos profundos con algunas sim ple modelos (LR, RF, XGB, LGB). Los experimentos muestran que si se fija el umbral en 0,25 puede equilibrar los resultados de 0/1 y da los mejores resultados.

## ¿Con qué clase de palabratrabaja? 
*Trabajan con palabras léxicamente plenas*

# Sentence Similarity Learning by Lexical Decomposition and Composition
## ¿Qué hace? 
El objetivo es evaluar la similitud de oraciones para determinar si dos oraciones son paráfrasis o no. 
En este trabajo, proponemos un modelo para evaluar la similitud de las frases mediante la descomposición y composición de la semántica léxica.

## ¿Cómo lo hace? 

En este artículo, proponemos un modelo novedoso para abordar todos estos retos de forma conjunta, descomponiendo y descomponiendo y componiendo la semántica léxica de las frases. Dado un par de frases, el modelo representa cada palabra como un vector de baja dimensión (reto 1), y calcula un vector de correspondencia semántica para cada palabra basado
en todas las palabras de la otra frase (reto 2). A continuación, basándose en el vector de coincidencia semántica, cada vector de palabras vector de palabras se descompone en dos componentes: un componente similar y un componente disímil (reto 3). Utilizamos los componentes similares de todas las palabras para representar las partes similares de la pareja de frases, y los componentes dis similares de cada palabra para modelar explícitamente las partes disímiles. A continuación, se realiza una operación de CNN de dos canales de dos canales para componer los componentes similares y disimilares en un vector de características (desafío 2 y 3). Por último, el vector de características compuesto se utiliza para predecir la similitud de la frase. Los resultados experimentales en dos tareas muestran que nuestro modelo obtiene el rendimiento más avanzado en la tarea de selección de frases de respuesta, y logra un resultado comparable en la tarea de identificación de paráfrasis.
En las siguientes partes, comenzamos con una breve descripción de nuestro modelo (Sección 2), seguida de los detalles de nuestra implementación de extremo a extremo (Sección 3). A continuación, evaluamos nuestro modelo en las tareas de selección de frases de respuesta y la identificación de paráfrasis (Sección 4).


En este trabajo, proponemos un modelo para evaluar la similitud de las frases mediante la descomposición y composición de la semántica léxica. Para resolver el problema de la brecha léxica, nuestro modelo representa cada palabra con su vector de contexto. Para extraer características tanto de la similitud como de la disimilitud de un par de oraciones, diseñamos varios métodos para descomponer el vector de palabras en un componente similar y un componente disímil. Para extraer características a múltiples niveles de granularidad, empleamos un modelo CNN de dos canales y lo equipamos con múltiples tipos de filtros de ngramas. Los resultados experimentales muestran que nuestro modelo es bastante eficaz tanto en la tarea de selección de frases de respuesta como en la de identificación de paráfrasis.
## ¿Con qué clase de palabratrabaja? 
*Trabajan con palabras léxicamente plenas*



Conclusión: 

