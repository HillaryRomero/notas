
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
## ¿Cómo lo hace? 
## ¿Con qué clase de palabratrabaja? 


# Learning Semantic Hierarchies via Word Embeddings
## ¿Qué hace? 
## ¿Cómo lo hace? 
## ¿Con qué clase de palabratrabaja? 


# Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking
## ¿Qué hace? 
## ¿Cómo lo hace? 
## ¿Con qué clase de palabratrabaja? 


# Sentence Similarity Learning by Lexical Decomposition and Composition
## ¿Qué hace? 
## ¿Cómo lo hace? 
## ¿Con qué clase de palabratrabaja? 





Conclusión: 

