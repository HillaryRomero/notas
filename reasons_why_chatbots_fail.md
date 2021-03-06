# reasons_why_chatbots_fail
La principal razón por la que los chatbots han fallado se debe a la capacidad reducida de comprender el lenguaje. El desarrollo de la comprensión del
lenguaje natural ha sido progresivo, sin embargo, ha tardado más tiempo qde lo esperado.
A pesar de que algunos modelos han logrado grandes avances, su versatilidad no se ha desarrollado de manera óptima. 


# Problemas
Problemas en la comprensión de las oraciones humanas:
- Capacidad muy reducida de comprender el contexto.
- Capacidad reducida de comprender la intención del usuario.
- Capacidad reducida para  manejar la necesidad del usuario y así darle una experiencia natural a la conversación. 
- Dificultad en la toma de una decisión para ayudar al usuario. 
- Dificultad para procesar ironía o situaciones de la vida diaria.


# Ventajas
- Integraciones con aplicaciones de mensajería. Evita que los usuarios se vean en la obligación de descargar una aplicación alternativa para hacer uso del chatbot. 
- Reducen el trabajo manual. 
- Facilitan la recolección de datos.
- Facilitan el análisis de datos.
- Usan AI. Capacidad de alimentarse del conocimiento que reciben cada día. 


# Desventajas
- Dificultad para predecir consultas. 
- Información sensible (imposibilidad de automatizar algunas respuestas por tratarse de asuntos particulares. Ej: temas médicos o personales).
- Poca flexibilidad.
- Pérdida de datos.
- Rechazo de los usuarios. 
- Carencia de emociones.


# Ideal
Las versiones más sofisticadas deberían detectar dudas en función de las acciones de los usuarios, 
recordar el contexto, etc. 

# Alcance actual
Tienen la capacidad de asumir cualquier tarea que no requiera un conocimiento muy específico y una toma de decisiones
espontánea.


# Chatbots exitosos 
1. H&M Bot
2. KLM 
3. Lemonade
4. Around Me
5. Insomnobot de Casper 


# Razón del éxito de estos chatbots
- Obteniendo aprendizajes para ir adaptando sus contenidos (incorporan machine learning para mejorar la experiencia de sus usuarios).
- Optimizando procesos complejos desde la conversación.
- Creando escenarios conversacionales basados en el momento del día (analizan el comportamiento y los patrones de uso de sus usuarios).


# Criterios determinados por los usuarios para considerar que un chatbot es útil:
- Útil: *¿Está el chatbot resolviendo un problema que ya estaba confrontando el negocio y sus clientes antes? ¿Es una solución viable?*
- Conversacional: *¿Las conversaciones fluyen y suenan humanas? ¿Tiene el chatbot sentido del humor? ¿Puede comprender a pesar de errores de ortografía y jerga?*
- Fácil de usar: *¿Necesitas registrarte/descargar/instalar algo para usar el chatbot? ¿Es gratis o tiene condiciones? ¿Tiene un buen diseño para poder usarlo fácilmente?*

# Nota final: 
Al partir del survey realizado, se desprenden temas comunes sobre los chatbots que, al parecer, no han sido abordados de una manera óptima y que pueden resultar de nuestro interés. Por ejemplo: el manejo del contexto, la intención del usuario, manejo de la necesidad del usuario y procesamiento de la ironía.

# Consultas: 
https://www.multiplica.com/conocimiento/articulos/5-ejemplos-exitosos-de-chatbots-y-como-replicarlos/
https://www.novicell.es/es/blog/chatbots-donde-fallan/
https://www.liveperson.com/blog/top-5-reasons-chatbots-fail
https://platinumpartner.com.au/chatbots-fails-reason/
https://blog.happyfox.com/7-reasons-chatbots-fail-and-how-we-can-fix-it/
https://www.socialmediatoday.com/news/the-key-challenges-and-benefits-of-utilizing-chatbots-for-business-infogra/594486/#:~:text=One%20of%20the%20major%20challenges,transactions%20or%20offer%20personalized%20experiences.
https://medium.com/@botsideapp/3-major-problems-with-chatbots-and-chatbot-development-503d84e176aa
https://theappsolutions.com/blog/development/challenges-of-chatbots-for-business/
https://programmerclick.com/article/97261115645/
https://www.comunicae.es/nota/si-un-bot-no-logra-generar-un-vinculo-1222664/
https://expansion.mx/tecnologia/2017/03/28/un-ano-despues-los-bots-no-son-tan-inteligentes
https://blogcandidatos.springspain.com/transformacion-digital/apocalipsis-de-ia-y-chatbot-es-tan-malo-como-crees/
IMPORTNTE PARA PENSAR EN PRUEBAS: https://www.nuance.com/content/dam/nuance/es_es/collateral/enterprise/ebook/eb-chatbot-fixes-and-fails-es-es.pdf
https://blog.cliengo.com/ventajas-desventajas-chatbot/
https://zyxme.com/blog/6-exitosas-empresas-que-integraron-chatbots-a-sus-canales-digitales/
https://www.zendesk.com.mx/blog/chatbot-para-empresas/
https://www.userlike.com/es/blog/los-mejores-chatbots
https://blog.cliengo.com/ventajas-desventajas-chatbot/
https://blog.laboremia.com/pa/ventajas-y-desventajas-de-los-chatbots-para-las-empresas
https://www.inbenta.com/es/blog/chatbots-buenos-o-malos-imitadores-de-la-interaccion-humana/



# Pruebas

**Crear pruebas que permitan aprender el contexto**

Pruebas para el modelo: 
- Crear pruebas que permitan evaluar si un modelo es capaz comprender el contexto:

En vista de que los chatbots actualmente pueden analizar las palabras de forma individual, pero -todavía- no pueden analizar el contexto, podríamos diseñar algunas pruebas enfocadas en enseñar: 
1. Las diversas interpretaciones de una misma frase.
2. Los diversos significados de una misma oración dentro de una frase. 
3. Los diferentes significados de una palabra específica en diversos contextos. 



**Opción 1**
La idea sería desarrollar un corpus que contengan entre 20 y 30 oraciones simples, donde cada una de ellas, sin convertirse en paráfrasis, pueda tener varias interpretaciones diferentes. 

Ej: 
Frase 1: *Ella nunca dijo que lo amaba.*

Interpretaciones: 
1. ELLA nunca le dijo que lo amaba.  (Pero otra persona sí lo dijo).
2. Ella NUNCA le dijo que lo amaba.  (Ninguna vez durante toda su relación).
3. Ella nunca le DIJO que lo amaba.  (Lo demostraba, pero nunca lo dijo en voz alta). 
4. Ella nunca LE dijo que lo amaba.  (No a él, pero sí se lo dijo a todos los demás).
5. Ella nunca le dijo que [ELLA] lo amaba. (Pero que otra persona sí)
6. Ella nunca le dijo que lo AMABA.  (Solo que le gustaba y que le parecía divertido).
7. Ella nunca le dijo que LO amaba. (Dijo que amaba a otra persona).

Creo que de esta forma podríamos enseñar las diversas interpretaciones que puede tener una misma frase. 

**Opción 2**
Crear un corpus que contenga entre 20 y 30 frases sencillas, comprendidas por varias oraciones, donde al menos en cada frase se repita una misma oración, y que esa oración tenga significados diferentes dentro de cada uno de los contextos.

Frase 1: *Él está sufriendo.* 

1. Este semestre Juan tiene cinco clases y todas son muy difíciles. Este semestre *él está sufriendo*.  
2. La suegra Juan al fin hoy se regresa a España. Segurito que *él está sufriendo*. 

**Opción 3**
Otra opción sería desarrollar un corpus que contengan un total de 30 oraciones. Cada una de estas oraciones contenndría una palabra que pueda ser ambigua dependiendo del contexto. 

Palabra 1: **banco*
1. El Banco de Inglaterra mantiene los tipos de interés en el 5,25%.
2. El anciano se sentó en un banco para descansar.
3. Al cruzar el puente los niños vieron un banco de peces.

# Comentarios
1. ¿Qué se entiende por "el chatbot fracasó"? La respuesta a esta pregunta puede tener perspectivas comerciales, de "lógica de negocios", de diseño o de tecnología. Valdría la pena limitar aquí si se va a tomar una o varias de estas perspectivas. ¿Por qué? Porque un chatbot puede fracasar simplemente porque la tecnología no da para más, o porque se intentó utilizar uno en una situación inapropiada. Sugeriría tener bien claro aquí el concepto de interfaz de usuario.

Por problemas con experiencia de usuario. La interfaz influye pero la experiencia de uso, las naturalidad de la conversación y la comodidad del usuario en el proceso comunicativo es importante. El dilema entre UX (User Experience) y UI (User Interface) . 

	
2. Si hay dificultades tecnológicas, ¿por qué sí hay chatbots que han realizado funciones de forma satisfactoria?
	
3. ¿Qué papel tendría la facilidad en la construcción y diseño del chatbot en su probabilidad de éxito?
	
4. ¿Qué quiere decir exactamente aquí el término "contexto"?
	
5. ¿Consideras que el emparejamiento de lo que se dice con el "intent" es suficiente para hablar de una interpretación semántica de los enunciados?
	
6. ¿Vamos a hacer recomendaciones prescriptivas o vamos a hacer un trabajo descriptivo? O sea, ¿vamos a decir que un chatbot falla si no consigue X, Y o Z (justificadas) o vamos a diseñar un mecanismo para observar el comportamiento de un chatbot dados los estímulos A, B o C? Se parecen en este caso, pero siempre hay una pequeña diferencia en el enfoque que puede cambiar el diseño de la investigación. Ambas perspectivas son válidas, ojo.

La última pregunta me resulta crucial. Tenemos dos caminos: uno es decir "como lingüista, me parece que un chatbot funcional debería manejar estas cualidades que maneja un ser humano" y si no lo hace no se acerca a un ideal. El otro camino -el descriptivo- podría ser comparar varias facetas de chatbots exitosos con los que no lo son a ver si encontramos algo que los distinga (sin pensar en el desarrollo de tecnologías futuras, por ejemplo); sería un poco ver lo que hay (con todo y sus limitaciones) y ver cómo aprovechar lo que tenemos para construir buenos chatbots.

Razones por las cuales fracasan los chatbots


# Solución de comentarios: 

# Tópico: Razones por las cuales fracasan los chatbots

# Introducción 
Según (Lexico Dictionaries, 2019) la definicón de chatbot hace refencia a: «A computer program designed to simulate conversation with human users, especially over the Internet» . Los chatbots han sido usados en diversos campos como: la educación, los negocios y el comercio electrónico, la salud y el entretenimiento. La motivación más importante en el uso de los chtabots guarda estrecha relación con el nivel de productividad o eficienca que el agente posea. Sin embargo, la productividad o eficiencia de estos agentes dependerá tanto de factores técnicos, como de factores empresariales o de la experiencia de usuario. 
 
Ahora, cuando la motivaicón de los usuarios decae y los chatbots resultan ser poco útiles, podríamos decir que un chatbot fracasó. En particular, abordaremos el estudio de **el fracaso** de los chatbots a partir de la expericiencia de usuario, donde un chatbot no es capaz de establecer una comunicación adecuada y eficiente con los usuarios. 
Así pues, para efectos de nuestra investigación, definiremos **el fracaso de un chatbot** como **la incapacidad del manejo lingüístico** que poseen los chatbots para comunicarse **de manera adecuada y eficiente** con los usuarios. Entiéndase **adecuada y eficiente** como: **la capacidad de procesar el lenguaje, comprender el contexto de la conversación y manejar las necesidades de los usuarios, ofreciendo una experiencia lo más natural posible, asemejándose a la interacción entre humanos.**

En resumen, consideraremos **el fracaso de un chabot** desde la **incapacidad del manejo lingüístico** que pueden tener estos agentes y cómo esta incapacidad afecta la motivación en el uso de los mismos.


# Problema
Un estudio consultado destaca que «un chatbot exitoso, desde la perspectiva del usuario, es aquel capaz de realizar de manera eficiente y satisfactoria conversaciones más largas con un usuario» (Antje Janssen, Lukas Grützner, Michael H. Breitner). Sin embargo, el estudio también define **el éxito de los chatbots** como «un chatbot que está en funcionamiento y disponible, realiza las tareas para las que está diseñado y satisface a los usuarios». Esta definición deja parcialmente de lado lo que ellos llaman CFS's (Critical Success Factors for People) puesto que la disponibilidad del chatbot y la ejecución eficiente de tareas «son los pocos requisitos esenciales que deben funcionar perfectamente para que el chatbot tenga éxito» (Rockard 1979; Bullen y Rockard 1981). 

Otro estudio agrega que «para que los chatbots se adapten a las necesidades de usuarios y contextos conversacionales específicos, es probable que sea necesario mejorar los modelos de usuario y de contexto. Los chatbots y sus interacciones con los humanos deben ser analizados y rediseñados, no sólo preocupándose por las secuencias de interacción específicas, sino también con el objetivo de mejorar las respuestas generativas a las entradas de una serie de usuarios dentro de una variedad de contextos conversacionales» (Petter Bae Brandtzaeg, Asbjørn Følstad). 

Sin embargo, al consultar sitios web que recogen criterios determinados por los usuarios para considerar que un chatbot es útil, pudimos notar que los usuarios consideran que las versiones más sofisticadas de los chatbots deberían recordar el contexto, detectar dudas en función de las acciones de los usuarios, entre otros.
Y ya que resulta de interés el asunto sobre el contexto, debido a que es fundamental para los usuarios; en nuestro caso particular, entenderemos por contexto: **una serie de elementos semánticos que hayan sido nombrados por el usuario en la conversación**. 


# Objetivo
De esta revisión se desprenden dos posibles objetivos: 

1. Un estudio prescriptivo que permita, desde una perspectiva lingüística, crear criterios para medir si un chatbot es funcional o no. Entiéndase funcional en este contexto como ser capaz de manejar en una conversación cualidades que maneja un ser humano.  
2. Un estudio descriptivo que permita diseñar un mecanismo para observar el comportamiento de un chatbot dados algunos estímulos. Con este mecanismo podremos comparar varias facetas de chatbots exitosos con los que no lo son y evaluar si encontramos rasgos distintivos. 


# Evaluación
1. Para el estudio prescriptivo: 
- Reuniremos y reorganizaremos los problemas encontrados que guarden relación con el tópico que investigamos. 
- Estableceremos una serie de criterios que incluyan justificaciones lingüísticas acerca de lo que calificaremos como un chatbot funcional frente a uno no funcional. 
- Los criterios anteriormente mencionados servirán como herramienta para medir la funcionalidad de un chatbot.

2. Para el estudio descriptivo: 
- Seleccionaremos 5 chatbots de un mismo rubro.
- Desarrollaremos un corpus que contenga 10 escenarios complejos.
- Introduciremos un total de 10 escenarios, por conversación, a cada uno de los chatbots seleccionados. 
- Introduciremos los escenarios uno a uno. Estos escenarios serán facilitados en el mismo orden para cada uno de los casos. 
- Evaluaremos cómo se comportan cada uno de estos chatbots del mismo rubro, obteniendo las mismas entradas en una conversación. 
- Observaremos, desde una perspectiva lingüística, hasta dónde es capaz de llegar cada chatbot en la conversación. 




> ### Sources:
> 1. Why do Chatbots fail? A Critical Success Factors Analysis: (Antje Janssen, Lukas Grützner, Michael H. Breitner)
> https://www.researchgate.net/profile/Antje-Janssen/publication/354811221_Why_do_Chatbots_fail_A_Critical_Success_Factors_Analysis/links/614dbb5a154b3227a8a62ecc/Why- do-Chatbots-fail-A-Critical-Success-Factors-Analysis.pdf 
> "We define success of chatbots from the organizational and main responsible managers’ point of view by the fact that a chatbot is functioning and available, performs > the tasks for which it is designed, and satisfies the users of a chatbot" (CFS's = Critical Success Factors for People). 
> whereas CSFs are the few essential requirements that must run perfectly to be successful with the chatbot (Rockard 1979; Bullen and Rockard 1981). 
>
> 2. Chatbots: History, technology, and applications: (Eleni Adamopoulou,Lefteris Moussiades)
>  https://www.sciencedirect.com/science/article/pii/S2666827020300062
>
> 3. Chatbots: changing user needs and motivations: (Petter Bae Brandtzaeg, Asbjørn Følstad)
 https://dl.acm.org/doi/fullHtml/10.1145/3236669?casa_token=gmu4Oj9kvLUAAAAA:5PWolkbbrkGsWXoRait-EY7UwWAdHoPbzORkWsNwgh27jnu8IjOmmRj4SyM3hjU4zaZXeiTwTg0BQlU
>
> 4. Customer service chatbots: Anthropomorphism and adoption: (Ben Sheehan, Hyun Seung Jin, Udo Gottlieb)
> https://www.sciencedirect.com/science/article/pii/S0148296320302484?casa_token=BL8BrKJFrXMAAAAA:R7DccQhF_1zgI-xmB0ZqgyGObWHjVsAA2eA88UvkXQmEc7SnyUaX8nm8NvEAYXivn9iQ9efl1zTA


## Párrafo de respaldo
Así pues, para efectos de nuestra investigación, definiremos **el fracaso de un chatbot** como **la incapacidad del manejo lingüístico** que poseen los chatbots para comunicarse **de manera adecuada y eficiente** con los usuarios. Entiéndase **adecuada y eficiente** como: «la capacidad de procesar el lenguaje, comprender la intención del usuario y manejar las necesidades de los mismos, ofreciendo una experiencia lo más natural posible, asemejándose a la interacción entre humanos.»

1. Para el estudio prescriptivo : 
(Reunir y organizar los problemas encontrados + crear una herramienta que permita medir si el chatbot es bueno manejando capacidades linguistcicas como la compresión del  contexto. 
2. Un estudio descriptivo (contrastar X número de chatbot con X cantidad de escenarios y facilitarle estas oraciones en el mismo orden y ver hasta dónde es, cada cchatbot, capaz de comunicarse eficientemente y comprender el contexto)



# Resumen

Hice una revisión acerca de: **las razones por las cuales fracasan los chatbots**
Abordando **el fracaso de los chatbots a partir de la experiencia de usuario**, donde un chatbot no es capaz de establecer una comunicación adecuada y eficiente con los usuarios. 
En este caso particular, definimos **el fracaso de un chatbot** como **la incapacidad del manejo lingüístico** que poseen los chatbots para comunicarse de manera adecuada y eficiente con los usuarios. Entendiendo aquí adecuada y eficiente como: **la capacidad de procesar el lenguaje, comprender el contexto de la conversación, ofreciendo una experiencia lo más natural posible.**
Consideraremos el fracaso de un chatbot desde la incapacidad del manejo lingüístico que pueden tener estos agentes y cómo esta incapacidad afecta la motivación en el uso de los mismos.

Para delimitar la investigación y debido a que es fundamental para los usuarios, la propuesta está enfocada a lo que es la comprensión del contexto. Entendiendo por contexto: **una serie de elementos semánticos que hayan sido nombrados por el usuario en la conversación.**

**A partir de esta revisión, se desprenden dos posibles objetivos:**
1. Un estudio prescriptivo que permita, desde una perspectiva lingüística, crear criterios para medir si un chatbot es funcional o no. Entiéndase funcional en este contexto como ser capaz de manejar en una conversación cualidades que maneja un ser humano.  

2. Un estudio descriptivo que permita diseñar un mecanismo para observar el comportamiento de un chatbot dados algunos estímulos. Con este mecanismo podremos comparar varias facetas de chatbots exitosos con los que no lo son y evaluar si encontramos rasgos distintivos. 




**Determinar la incidencia del contexto cognitivo en el éxito/fracaso de los chatbots como experiencias de usuario**

**Objetivo 1:** determinar de forma prescriptiva la relación lingüística entre el uso apropiado del contexto (memoria/conocimiento) y la performance de un chatbot; comparar este ideal con 5 chatbots comerciales considerados exitosos.
**Entregable 1:** artículo en el que se presenten los resultados cualitativos de la comparación entre los 5 chatbots y el ideal; recomendaciones.

**Objetivo 2:** evaluar el desempeño de 5 chatbots comerciales de propósito similar a partir de algunos escenarios en los que se requiera del uso del contexto para poder interpretar adecuadamente los inputs del usuario.
**Entregable 2:** artículo con la comparación de éxito/fracaso para los chatbots.



# ¿Qué significa contexto de la conversación en estas investigaciones?  

**1. Why do Chatbots fail? A Critical Success Factors Analysis**
https://www.researchgate.net/profile/Antje-Janssen/publication/354811221_Why_do_Chatbots_fail_A_Critical_Success_Factors_Analysis/links/614dbb5a154b3227a8a62ecc/Why-do-Chatbots-fail-A-Critical-Success-Factors-Analysis.pdf

**Context = intent. No hablan del contexto directamente, hablan del intent. Y definen el problema central como la incapacidad para interpretar la intención del usuario o proporcionar respuestas adecuadas**

While the development, release, and deployment of chatbots is largely reported in scientific literature and practitioner reports, there are only isolated reports of failed chatbots, such as the Microsoft chatbot Tay (Brandtzaeg and Følstad 2018). From a user perspective, several researchers define chatbot failure within
a human-to-chatbot interaction in the form of conversation irregularities, i.e., the chatbot's inability to perform tasks for the user through its inability to either interpret the intent or to provide proper responses (Filipczyk et al. 2016; Seeger and Heinzl 2021; Mozafari et al. 2021). From a more global perspective, we
expand the chatbot failure definition by also including chatbots that have been discontinued by being taken offline.

**3. Chatbots: changing user needs and motivations:**
**Context = No definen el contexto como tal. Solo lo mencionan, dicen que hay que mejorar los moldelos de usuario y de contexto. Y hablan de la posible variación imprevisible de las entradas de los usuarios **  

Chatbots in general, and in particular, AI-powered chatbots, need substantial adaptation and maintenance to perform their task properly. The potential unpredictable variation in user input, as demonstrated in the chatbot failures above, and what constitutes a valid chatbot response, represent substantial challenges for the HCI field. In order to develop chatbots that adapt to the needs of specific users and conversational contexts, there is likely a need for improved user and context models. Chatbots and their interactions with humans must be analyzed and redesigned, not only with concern for specific interaction sequences, but also with the aim of improving generative responses to inputs from a range of users within a variety of conversational contexts.

**4. Customer service chatbots: Anthropomorphism and adoption**
**Context = Se dice que el contexto local que se trata de un significado compartido derivado temporalmente, de enunciados cinco turnos antes o después del presente
enunciado **

Se dice que el contexto local que se trata de un significado compartido derivado temporalmente, de enunciados cinco turnos antes o después del presente
enunciado. Por el contrario, el contexto global es el producto de todos los enunciados de una conversación, así como de una conversación, así como las dimensiones situacionales que rodean el acto comunicativo, como elcultural del interlocutor o el entorno en el que se produce el acto.

Local context is said to be shared meaning derived temporally, from utterances five turns before or after the present
utterance. Conversely, global context is the product of all utterances from a conversation as well as situational dimensions surrounding the communicative act, such as an interlocutor’s cultural background or the environment in which the act occurs.


# Plan para pruebas
¿A qué hora sale mi viaje? / ¿Cuál es la hora de salida de mi vuelo? 
¿Cómo puedo pagar pasaje? / ¿De qué forma puedo pagar mi boleto?
¿Cuáles son los detinos más recomendados para viajar durante el verano? / ¿Qué rutas lugares recomiendas para viajar en el verano?
¿Hay vuelos habilitados los fines de semana? / ¿Hay vuelos disponibles los sábados y domingos? 





