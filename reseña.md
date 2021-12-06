En los recientes artículos revisados fue posible observar que, si bien hay un gran número de estudios sobre semántica y word embeddings, los experimentos en dichos
papers revisados se enofocan en trabajar con palabras léxiacemente plenas. Es probabeble que existan estudios de palabras funcionales, semántica 
y word embbedings pero puede que sean escasos.  

En líneas generales, los estudios revisados tienen como objetivo lo siguiente: 

#### 1. Adjusting Word Embeddings with Semantic Intensity Orders:
- **a.** Buscan acercar las palabras semánticamente cercanas y alejar las semánticamente distantes,
manteniendo los vector de palabras sin alejarse demasiado de la posición original.
- **b.** Parten de uno de los tres tipos de vectores de palabras disponibles como base para sus estudios: GloVe, CBOW y Paragram-SL999
(Wieting et al., 2015); y ajustan cada uno de estos conjuntos de vectores con una variedad de métodos contrastivos. 
- **c.** Trabajan con palabras léxicas: sinónimos, antónimos, hiperónimos.

#### 2. DecodingWord Embeddings with Brain-Based Semantic Features
**a.** Buscan decodificar el contenido de las word embeddings mapeándolas en vectores de características semánticas interpretables para
 (i) identificar qué rasgos semánticos están mejor codificados en las incrustaciones de palabras;
 y (ii) utilizar las representaciones de rasgos propuestas para explicar el rendimiento de las incrustaciones en tareas de sondeo semántico.
**b.** Prueba el método de decodificación de incrustaciones en varios tipos de MDS estáticos y contextualizados. 
Todos los modelos logran altas correlaciones entre las palabras y los rasgos, y los MDS basados en la dependencia tienen una ligera ventaja
sobre los demás, en consonancia con los hallazgos de Abnar et al. (2018).
También han aplicado las representaciones de rasgos descodificados a la metodología de la probing task,
para conocer qué piezas de información semántica captan realmente los probing classifiers.
**c.** Trabajan con palabras léxicas: adjetivos positivos y negativos, sustantivos concretos y asbtractos, animados e inanimados y verbos.

#### 3. Improving Lexical Embeddings with Semantic Knowledge
**a.** Buscan demostrar el valor del aprendizaje de incrustaciones semánticas con información de recursos semánticos.
**b.** En cada escenario, compararemos la incrustación de base de word2vec entrenada con cbow contra RCM solo, el modelo conjunto y Joint -- RCM.
Consideran tres tareas de evaluación: el modelado del lenguaje, la medición de la similitud semántica y la predicción de los juicios humanos 
sobre la relación semántica.
llevan a cabo el desarrollo del modelo y ajustan los parámetros del mismo (C, cbow, RCM, conjunto de datos PPDB, etc.) en los datos de desarrollo, y evalúan s el modelo
de mejor rendimiento en los datos de prueba. ¡Los modelos se denominan de la siguiente manera: word2vec para el objetivo de referencia (cbow o skip-gram), RCM-r/p y Joint-r/p para 
inicializaciones aleatorias y preentrenadas de los objetivos RCM y Joint, y Join RCMt! para el preentrenamiento de RCM con incrustaciones conjuntas.
**c.** Trabajan con palabras léxicamente plenas (indirectamente). 

#### 4. Learning Semantic Hierarchies via Word Embeddings
**a.** El objetivo es entrenamiento de la incrustación de palabras, el aprendizaje de la proyección y la identificación de la relación entre hiperónimos-hipónimos. 
**b.** Este artículo propone un método novedoso para la construcción de jerarquías semánticas basado en la incrustación de palabras, que se entrena utilizando un corpus a gran escala. 
A partir de las incrustaciones de palabras, aprendemos la relación hipernimia-hipónimo mediante la estimación de matrices de proyección que asignan las palabras a sus hipérnimos.
Se introducen nuevas mejoras mediante un enfoque basado en clústeres para modelar las relaciones más precisas. A continuación, proponemos unos criterios sencillos para identificar 
si un nuevo par de palabras es una relación hipernímico-hipónima. A partir de las relaciones hipernímicas-hipónimas por pares, construimos automáticamente jerarquías semánticas.
En nuestros experimentos, el método propuesto supera significativamente a los métodos más avanzados y alcanza la mejor puntuación F1 del 73,74% en un conjunto de datos de prueba
etiquetados manualmente. 
**c.** Trabajan con palabras léxicamente plenas. 

#### 5. Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking 
**a.** El objetivo es el Emparejamiento semántico para determinar la similtud entre textos. También proponen una nueva arquitectura para resolver este problema, 
denominada modelo DMPSM. En detalle, su modelo obtiene información de multipercepción, el significado semántico de toda la frase y la característica de 
interacción de las palabras, lo que ayuda a conseguir la mejor puntuación.
**b.** Utilizan CNN para capturar convenientemente la característica de N-gramas mediante núcleos de tamaño múltiple que que ayudarán a emparejar 
la frase en diferentes granularidades. El modelo observa una frase desde un punto de vista vi sual de vista, e ignora la relación secuencial 
de las palabras hasta cierto punto. También usan  LSTM para el modelo de lenguaje, y es bueno para modelar la formación de secuencias. Además usan otros modelos en combinación 
para  la de codificación de frases y la interacción. 
**c.** Trabajan con palabras léxicamente plenas.


#### 6. Sentence Similarity Learning by Lexical Decomposition and Composition

**a.** El objetivo es evaluar la similitud de oraciones para determinar si dos oraciones son paráfrasis o no. En este trabajo, proponemos un modelo para evaluar la similitud de las frases mediante la descomposición y composición de la semántica léxica. 
**b.** Dado un par de frases, el modelo representa cada palabra como un vector de baja dimensión (reto 1), y calcula un vector de correspondencia semántica para cada palabra basado en todas las palabras de la otra frase (reto 2). A continuación, basándose en el vector de coincidencia semántica, cada vector de palabras vector de palabras se descompone en dos componentes: un componente similar y un componente disímil (reto 3).
Utilizan los componentes similares de todas las palabras para representar las partes similares de la pareja de frases, y los componentes disimilares de cada palabra para modelar explícitamente las partes disímiles. A continuación, se realiza una operación de CNN de dos canales de dos canales para componer los componentes similares y disimilares en un vector de características (desafío 2 y 3). Por último, el vector de características compuesto se utiliza para predecir la similitud de la frase. Los resultados experimentales en dos tareas muestran que el modelo obtiene el rendimiento más avanzado en la tarea de selección de frases de respuesta, y logra un resultado comparable en la tarea de identificación de paráfrasis.
**c.** Trabajan con palabras léxicamente plenas.


que no hay nada que haya discriminado entre palabras funcionales/plenas en lo que has revisado (por lo menos de forma directa).
Indirectamente, si algo utilizó wordnet, trabajó con palabras léxicas.
