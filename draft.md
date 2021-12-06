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


*Trabajaron con palabras léxicas: sinónimos, ant´nimos, hiperonimos.*


# 5. DecodingWord Embeddings with Brain-Based Semantic Features

# EN
In this article, we have taken a different route, adopting a methodology inspired
by the literature on neural decoding in cognitive neuroscience. The brain, too, represents semantic information in distributed patterns (Huth et al. 2016). We argue that the problem of interpreting the content of embeddings is similar to interpreting the semantic content of brain activity. Neurosemantic decoding aims at identifying the information encoded in the brain by learning a mapping from neural activations to semantic features. Analogously, we decode the content of word embeddings by mapping them onto interpretable semantic feature vectors. Featural representations are well known
in linguistics and cognitive science (Vigliocco and Vinson 2007), and provide a
human-interpretable analysis of the components of lexical meaning. In particular, we rely on the ratings collected by Binder et al. (2016), whose feature set is motivated on a neurobiological basis. We have carried out the mapping of continuous embeddings onto discrete semantic features with a twofold aim:
 (i) identifying which semantic features are best encoded in word embeddings; and (ii) using the proposed featural representations to explain the performance of embeddings in semantic probing tasks.
Concerning the first goal, we have tested the embedding decoding method on
several types of static and contextualized DSMs. All models achieve high correlations across words and features, with dependency-based DSMs having a slight edge over the others, consistently with the findings of Abnar et al. (2018). 

The features from abstract domains such as Cognition, Social, and Causal seem to be the ones that are better predicted by the models, which are purely relying on text-based information, while the prediction of spatial and temporal features is obviously more challenging. A further analysis reveals the salience of visual, motion, and audition features, supporting the hypothesis that language redundantly encodes several aspects of sensory-motor information (Louwerse 2008; Riordan and Jones 2011). In terms of word categories, the vectors are very good in predicting entities, whereas they struggle with physical and
abstract properties. Moreover, it is interesting to observe that the new generation of semantic information they encode.
As for the second goal, we have applied our decoded feature representations to the widely popular probing task methodology, to gain insight on what pieces of semantic information are actually captured by probing classifiers. For our experiments, we tested the original embeddings on probing tasks designed to target affective valence, animacy, concreteness, and several verb classes derived from VerbNet for non-contextualized DSMs, and direct object animacy and causative/inchoative verb alternations for contextualized embeddings. If a binary classifier manages to identify whether a word belongs to a semantic class on the basis of its embedding, this is typically taken as indirect evidence that the embedding encodes the relevant piece of semantic information. In our
work, instead of regarding probing tasks just as “black box” experiments, we use the decoded feature vectors to inspect the semantic dimensions learned by the classifiers.
Moreover, we have set up a battery of tests to show how the decoded features can explain the embedding performances in the probing tasks. We have measured with AP the overlap between the top task features and the most important features of the test words belonging to the positive and negative classes. Our analyses reveal that:


the words correctly classified in the positive class (i.e., TPs) share a large
number of the top ranked features for that class, and, symmetrically,
the words correctly classified in the negative class (i.e., TNs) have a
significantly lower number of the top task features;
•
words wrongly classified in the negative class (i.e., FNs) lack many of the
top features characterizing the target class. Conversely, the features of
words wrongly classified in the positive class (i.e., FPs) tend to overlap
with the top task features more than TNs;
•
the accuracy of a DSM in a probing task strongly correlates with the
degree of separation between the semantic features decoded from its
embeddings of the words in the positive and negative classes.

These results show that semantic feature decoding provides a simple and useful tool to explain the performance of word embeddings and to enhance the interpretability of probing tasks.
The methodology we have proposed paves the way for other types of analyses
and applications. There are at least two prospective research extensions that we plan to pursue, respectively concerning selectional preferences and word sense disambiguation.
Many recent approaches to the modeling of selectional preferences have given
up on the idea of characterizing the semantic constraints of predicates in terms of discretesemantic types, focusing instead on measuring a continuous degree of predicate argument compatibility, known as thematic fit (McRae and Matsuki 2009). DSMs have been extensively and successfully applied to address this issue, typically measuring the cosine between a target noun vector and the vectors of the most prototypically predicate arguments (Baroni and Lenci 2010; Erk, Padó, and Padó 2010; Lenci 2011; Sayeed, Greenberg, and Demberg 2016; Santus et al. 2017; Chersoni et al. 2019; Zhang, Ding, and Song 2019; Zhang et al. 2019; Chersoni et al. 2020; Pedinotti et al. 2021). This approach can be profitably paired with our decoding methodology to identify the most salient features associated with a predicate argument. For instance, we can expect that listen selects for direct objects in which Audition features are particularly salient. This way, distributional methods will be able not only to measure the gradient preference of a predicate for a certain argument, but also to highlight the features that explain this preference, contributing to characterizing the semantic constraints of predicates.
As for word-sense disambiguation, models like ELMo and BERT provide con
textualized embeddings that allow us to investigate word sense variation in context. Using contextualized vectors, it might be possible to investigate how meaning changes in contexts by inspecting the feature salience variation of different word tokens. For example, we expect features like SOUND and MUSIC to be more salient in the vector of play in the sentence The violinist played the sonata, rather than in the sentence The team played soccer. This could be extremely useful also in tasks such as metaphor and token level
idiom detection, where it is typically required to disambiguate expressions that might have a literal or a non-literal sense depending on the context of usage (King and Cook 2018; Rohanian et al. 2020).
Word embeddings and featural symbolic representations are often regarded as
antithetic and possibly incompatible ways of representing semantic information, which pertain to very different approaches to the study of language and cognition. In this paper, we have shown that the distance between these two types of meaning representation is shorter than what appears prima facie. New bridges between symbolic and distributed lexical representations can be laid, and used to exploit their complementary strengths: The gradience and robustness of the former and the human-interpretability of the
latter. An important contribution may come from collecting more extensive data about feature salience. The Binder data set is an important starting point, but human ratings about other types of semantic features and words might be easily collected with crowd sourcing methods.
In this work, we have mainly used feature-based representations as a heuristic tool to interpret embeddings. An interesting research question is whether decoded features from embeddings could actually have other applications too. For instance, semantic features provide a more abstract type of semantic representation that might be complementary to the fine-grained information captured by distributional embeddings. This suggests to exploring new ways to integrate symbolic and vector models of meaning



Qué hicieron y cómo lo hicieron: 





*Trabajaron con palabras léxicas: adjetivos positivos y negativos, sustantivos concretos y asbtractos, animados e inanimados y verbos.*

# 8. Improving Lexical Embeddings with Semantic Knowledge

The goal of our experiments is to demonstrate the value of learning semantic embeddings with information from semantic resources. In each setting, we will compare the word2vec baseline embedding trained with cbow against RCM alone, the joint model and Joint -- RCM. We consider three evaluation tasks: language modeling, measuring semantic similarity, and predicting human judgements on semantic relatedness. In all of our experiments, we conducted model development and tuned model parameters (C, cbow, RCM, PPDB dataset, etc.) on development data, and evaluate the best performing model on test data. The models are notated as follows: word2vec for the baseline objective (cbow or skip-gram), RCM-r/p and Joint-r/p for random and pre-trained initializations of the RCM and Joint objectives, and Join RCMt!
for pre-training RCM with Joint embeddings. Unless otherwise notes, we train using PPDB XXL.
We initially created WordNet training data, but found it too small to affect results. Therefore, we include only RCM results trained on PPDB, but show evaluations on both PPDB andWordNet.


We trained 200-dimensional embeddings and used output embeddings for measuring similarity. During the training of cbow objectives we remove all
words with frequencies less than 5, which is the default setting of word2vec.

We conclude our experiments with an analysis of modeling choices. First, pre-training RCM models gives significant improvements in both measuring
semantic similarity and capturing human judgements (compare “p” vs. “r” results.) Second, the number of relations used for RCM training is animportant factor. Table 5 shows the effect on dev data of using various numbers of relations. While we see improvements from XL to XXL (5 times as many relations), we get worse results on XXXL, likely because this set contains the lowest quality relations in PPDB. Finally, Table 6 shows different
learning rates for the RCM objective.

The baseline word2vec and the joint model have nearly the same averaged running times (2,577s and 2,644s respectively), since they have same number of threads for the CBOWobjective and the joint model uses additional threads for the RCM objective. The RCM models are trained with single thread for 100 epochs. When trained on the PPDB-XXL data, it spends 2,931s on average.

*Trabajan con palabras léxicamente plenas*


# 9. Learning Semantic Hierarchies via Word Embeddings

In this section, we first define the task formally.
Then we elaborate on our proposed method composed of three major steps, namely, word embedding training, projection learning, and hypernym–
hyponym relation identification

Given a list of hypernyms of an entity, our goal is to construct a semantic hierarchy on it (Figure 1). We represent the hierarchy as a directed graph
G, in which the nodes denote the words, and the edges denote the hypernym–hyponym relations. Hypernym-hyponym relations are asymmetric and
transitive when words are unambiguous:

Here, L denotes the list of hypernyms. x, y and z, deonte hypernyms in L.
We use H to represent a hypernym–hyponym relation in this
paper. Actually, x, y and z are unambiguous as the hypernyms of a certain entity. Therefore, G should be a directed acyclic graph (DAG).



This paper proposes a novel method for semantic hierarchy construction based on word embeddings, which are trained using a large-scale corpus. Using the word embeddings, we learn the hypernym–hyponym relationship by estimating
projection matrices which map words to theirhypernyms. Further improvements are made using a cluster-based approach in order to model the more fine-grained relations. Then we propose a few simple criteria to identity whether a new word pair is a hypernym–hyponym relation. Based on the pairwise hypernym–hyponym relations, we build semantic hierarchies automatically.

In our experiments, the proposed method significantly outperforms state-of-the-art methods and achieves the best F1-score of 73.74% on a manually
labeled test dataset. Further experiments show that our method is complementary to the previous manually-built hierarchy extension methods


# 11. Semantic Matching Using Deep Multi-Perception Semantic Matching Model with Stacking
Sentence Pair Matching is a common task in NLP domain. The challenging of the semantic matching is that the matching requirements are different, and the definition of matching can be also flexible. Existing semantic models, such as Word2Vec, LDA, etc., can determine the similarity between text. But it is difficult to say whether the two paragraphs of text are saying ”the same thing”. For example, when we try to solve the classic sentence retelling problem, it is necessary to judge whether the two sentences are merely different in expression, but the meaning is the same.

However, as Quora question-matching corpus is published, a large number of sentence matching research work carried out the definition of the corpus publisher, which is called semantic equivalence discrimination, semantic equivalence judgment, or equivalent, rather than directly judge whether the two sentences have the same semantics, the core problem turn into the intent match of the sentence.

The Task 3 of China Conference on Knowledge Graph and Semantic Computing
(CCKS) 2018 is closer to the actual needs of NLP tasks such as smart customer service due to the data source is coming from real Q&A corpus. Given two sentences, the solution is supposed to determine whether the intentions are the same or similar. All corpora come from the real intelligent bank customer service log and have been screened and manually intent-matched.

In this paper, we not only implement various of deep semantic models, but also
propose a new architecture to solve this problem, called DMPSM model. In detail, our model obtains multi-perception information, whole sentence’s semantic meaning and words interaction feature, which help achieving the best score.

Because of the limited submission number, we only submitted and saved some deep model with better results. Other simple models with synthetic feature like Logistic Regression, Random Forest, XGBoost, LightGBM and also deep model InferSent are used in stacking to get better performance. Table 1 illustrates the results of different approaches. The analysis focus on two perspectives and it will help us find the best single
model architecture.

Which kinds of model can better obtain the semantic meaning of word se
quence?
CNN can conveniently captures N-gram feature by multi-size kernels which
will help matching sentence in different granularities. It looks at a sentence from a visual point of view, and ignores the sequence relationship of words to some extent. In contrast, LSTM is often used for language model, and good at modeling sequence information.
We can find that MPCNN get lower score than Bi-MPM Bi-LSTM or SSE,
and as lan et al[2] indicates that encoding sequential context information with LSTM is critical.

Which kinds of model is better, Sentence encoding model or Interaction model?
SSE model score is slightly lower than Bi-MPM, and it can be seen from the lan et al[2]’s analysis that the interactive model is generally better than encoding based model.
However, we can ignore which one is better. These two types of models solve problems from different angles, we combine the two ideas and propose the DMPSM model.
For better performance, we perform stacking on these deep models with some simple models (LR, RF, XGB, LGB). Experiments show that setting the threshold to 0.25 can balanced the 0/1 results and gives the best results.


Matching natural language text semantically is a key task for many applications in NLP. Different from semantic matching tasks based on common public data sets, our work pays more attention to the processing and understanding of real customer service data. With the in-depth study, we attempt multiple perspectives and ideas, which makes our research more practical and theoretical supported. Meanwhile, the implement of model fusion technique blends the viewpoint of different methods, from the experimental results, the method that this thesis puts forward comes to the result of our expectation.
Despite our many attempts and efforts, there is still room for improvement in accuracy.

Because of restrictions on data usage rules, we only train the word vector base on given training corpus, which led to the lacking of prior knowledge of professional field. In the future work, the introduction of knowledge graph of special domain may enhance the training efficiency. Furthermore, the other idea is taking advantage of model or knowledge from other areas and making more reasonable usage of these scarce data by transfer learning.


# 12. Sentence Similarity Learning by Lexical Decomposition and Composition



