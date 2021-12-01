RESUMEN: 
¿Qué buscan hacer? (Objetivo)
¿Cómo lo hacen? (Método)

# 3. Adjusting Word Embeddings with Semantic Intensity Orders
# EN
The common goal in these approaches is to make semantically close words closer and semantically distant words farther apart while keeping 
each word vector not to be too far from the original position. Although the joint training models can even indirectly adjust words that
are not listed in the semantic lexicons (Pham et al., 2015), the post-processing models are much more efficient and can be applied to word vectors
from any kinds of models, which can eventually perform better than the joint training models

GloVe vectors were used as the baseline. “base line” is compared to “same_ord (kmeans only)” in the first column and “syn&ant” is compared to
“syn&ant,same_ord,diff_ord(+kmeans)”. In both cases, we observe that some of the incorrectly judged pairs are corrected when adding the adjustment
with semantic intensity orders. In these cases, there were no pairs that were correctly judged by the adjustments without semantic intensity orders 
but incorrectly judged with semantic intensity orders.

In this work, we adjusted word vectors with inferred semantic intensity orders as well as information from WordNet and PPDB, 
and showed that adjusting word vectors with semantic intensity orders, synonyms, and antonyms altogether showed the best performance
for all the three datasets we evaluated on. Using the semantic intensity orders for adjusting word vectors can help represent 
semantic intensities of words in vector spaces. In addition, we showed the adjustments including semantic intensity orders are not 
harmful for the representation of semantics in general by evaluating on SimLex-999.
In future work, we plan to investigate clustering techniques beyond WordNet dumbbells and k means++ as preprocessing in the semantic ordering. 
The clusters using WordNet dumbbells depend on a preexisting semantic lexicon that may not cover all the semantically related words.
With k-means++, clusters may contain semantically opposite words and a word can belong to only one cluster.

# ES
## ¿Que buscan? 
El objetivo común de estos enfoques es acercar las palabras semánticamente cercanas y alejar las semánticamente distantes, 
manteniendo cada vector de palabras sin alejarse demasiado de la posición original. Aunque los modelos de entrenamiento 
conjunto pueden incluso ajustar indirectamente las palabras que no figuran en los léxicos semánticos (Pham et al., 2015),
los modelos de posprocesamiento son mucho más eficientes y pueden aplicarse a los vectores de palabras de cualquier tipo de modelos, 
que pueden llegar a obtener mejores resultados que los modelos de entrenamiento conjunto

Los vectores de GloVe se utilizaron como línea base. "línea base" se compara con "same_ord (kmeans only)" en la primera columna y "syn&ant" 
se compara con "syn&ant,same_ord,diff_ord(+kmeans)". En ambos casos, observamos que algunos de los pares juzgados incorrectamente se corrigen al añadir el ajuste
con órdenes de intensidad semántica. 
En estos casos, no hubo pares que se juzgaran correctamente con los ajustes sin órdenes de intensidad semántica pero que se juzgaran incorrectamente
con órdenes de intensidad semántica.

En este trabajo, ajustamos los vectores de palabras con órdenes de intensidad semántica inferidos, así como con información de WordNet y PPDB, 
y demostramos que el ajuste de los vectores de palabras con órdenes de intensidad semántica, sinónimos y antónimos en conjunto mostró el mejor rendimiento
para los tres conjuntos de datos que evaluamos. El uso de los órdenes de intensidad semántica para ajustar los vectores de palabras puede ayudar a representar
las intensidades semánticas de las palabras en los espacios vectoriales. Además, demostramos que los ajustes que incluyen órdenes de intensidad semántica no son 
perjudiciales para la representación de la semántica en general al evaluarlos en SimLex-999.
En futuros trabajos, planeamos investigar técnicas de clustering más allá de las mancuernas de WordNet y k means++ como preprocesamiento en el ordenamiento semántico.
Los clusters que utilizan las mancuernas de WordNet dependen de un léxico semántico preexistente que puede no cubrir todas las palabras semánticamente relacionadas. 
Con k-means++, los clusters pueden contener palabras semánticamente opuestas y una palabra puede pertenecer a un solo cluster.

## ¿Cómo lo consiguen?
En este estudio, partimos de uno de los tres tipos de vectores de palabras disponibles como base para nuestros estudios: GloVe, CBOW y Paragram-SL999
(Wieting et al., 2015); ajustamos cada uno de estos conjuntos de vectores con una variedad de métodos contrastivos.
Nuestro primer sistema contrastivo es una línea de base que utiliza sinónimos y antónimos ("syn&ant")
siguiendo el enfoque de Mrkši'c et al. (2016), que ajusta vectores de palabras para que la suma de las tres funciones objetivo de funciones objetivo de margen máximo se minimice.



# 5. DecodingWord Embeddings with Brain-Based Semantic Features

# 8. Improving Lexical Embeddings with Semantic Knowledge

# 9. Learning Semantic Hierarchies via Word Embeddings


# 10. Recent Trends in Deep Learning Based Natural Language Processing


# 11. Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking



# 12. Sentence Similarity Learning by Lexical Decomposition and Composition



