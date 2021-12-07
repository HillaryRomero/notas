En los recientes artículos revisados fue posible observar que, si bien hay un gran número de estudios sobre semántica y word embeddings, 
los experimentos en dichos papers revisados se enofocan en trabajar con palabras léxiacemente plenas.
Aunque hasta este momento y para nuestra comprensión no existen publicaciones sobre modelos que traten las palabras funcionales exclusivamente,
hay otros modelos que tratan la semántica de las palabras lexicamente plena con distintos métodos, entre ellos:

**Adjusting Word Embeddings with Semantic Intensity Orders (Joo-Kyung Kim†, Marie-Catherine de Marneffe‡, Eric Fosler-Lussier† , 2016).**
En este estudio buscan acercar las palabras semánticamente cercanas y alejar las semánticamente distantes, manteniendo los
vectores de palabras sin alejarse demasiado de la posición original. 

En otro estudio titulado **Learning Semantic Hierarchies via Word Embeddings (Ruiji Fu†, Jiang Guo†, Bing Qin†, Wanxiang Che†, Haifeng Wang‡, Ting Liu, 2014)** 
el objetivo es el entrenamiento de las word embeddings, el aprendizaje de la proyección y la identificación de la relación entre hiperónimos-hipónimos.

Adicionalmente en **Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking (Xu Cao, Xinran Liu, Binjun Zhu, Qingliang Miao,
Changjian Hu, Feiyu Xu, -no encontré el año-)** tienen como objetivo el emparejamiento semántico para determinar la similtud entre textos.
También proponen una nueva arquitectura para resolver este problema, denominada modelo DMPSM. En detalle, su modelo obtiene información de multipercepción,
el significado semántico de toda la frase y la característica de interacción de las palabras, lo que ayuda a conseguir la mejor puntuación.

Y finalmente en Sentence **Similarity Learning by Lexical Decomposition and Composition (ZhiguoWang and Haitao Mi and Abraham Ittycheriah, 2017)**
el objetivo es evaluar la similitud de oraciones para determinar si dos oraciones son paráfrasis o no.
En este trabajo, proponen un modelo para evaluar la similitud de las frases mediante la descomposición y composición de la semántica léxica.

En conclusión, parece que no hay nada que haya dado un trato diferente a palabras funcionales en lo que he revisado (por lo menos de forma directa).
En general, estos experimentos fueron trabajados con palabras léxicas. 




