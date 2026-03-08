[<<back](README.md)

# Definición de orientación a objetos según Alan Kays

> https://wiki.c2.com/?AlanKaysDefinitionOfObjectOriented

He estado pensando en poner esta página desde hace algún tiempo...

Mucho se menciona en [WardsWiki](https://wiki.c2.com/?WardsWiki) de la definición de OO promulgada por [Alan Kay](https://wiki.c2.com/?AlanKay), el inventor de [SmalltalkLanguage](https://wiki.c2.com/?SmalltalkLanguage). Muchos le consideran la voz más autorizada sobre [OO](https://wiki.c2.com/?DefinitionsForOo), ya uqe fue su inventor [HeInventedTheTerm](https://wiki.c2.com/?HeInventedTheTerm). (Otros no están de acuerdo, ese [FlameWar](https://wiki.c2.com/?FlameWar)).

La dificultad estriba en que no parece haber una fuente canónica para lo que Kay considera que es OO y no OO. Él ha escrito y dicho bastante, pero no hay ninguna referencia (que yo sepa) donde esté escrito. Además, sus pensamientos sobre el asunto parecen haber mutado un poco con el tiempo. Esto no es inusual ni incorrecto, ya que las personas modifican su forma de pensar cuando se les presentan nuevas evidencias. Pero hace que sea un poco difícil señalar un escrito en particular y afirmar cuál es la definición autorizada.

La referencia publicada más antigua conocida que podría revelar el pensamiento de Kay sobre el tema (que yo conozco, de todos modos) es el artículo [EarlyHistoryOfSmalltalk](https://wiki.c2.com/?EarlyHistoryOfSmalltalk) (que puede descargar yendo a esta [WikiPage](https://wiki.c2.com/?WikiPage)). Contiene la siguiente definición (en la página 78). Como se indica a continuación, esta es principalmente una descripción de Smalltalk

1. [TodoEsUnObjeto](https://wiki.c2.com/?EverythingIsAnObject).
2. Los objetos se comunican enviando y recibiendo mensajes (en términos de objetos).
3. Los objetos tienen su propia memoria (en términos de objetos).
4. Cada objeto es una instancia de una clase (que debe ser un objeto).
5. La clase mantiene el comportamiento compartido de sus instancias (en forma de objetos en una lista de programas)
6. Para evaluar una lista de programas, se pasa el control al primer objeto y el resto se trata como su mensaje.

Esta definición se deriva de las primeras versiones de Smalltalk (¿Smalltalk-72?), y las reglas 5 y 6 muestran claramente la herencia Lisp de Smalltalk. Kay comentó como tal, señalando que las reglas 4-6 mutarían a medida que se desarrollara Smalltalk.

**Objeción: en la página 78 se aclara que los anteriores son los principios de diseño detrás de Smalltalk, pero en ninguna parte se implica que también deban servir como la definición de [Orientado a Objetos](https://wiki.c2.com/?ObjectOriented)**.

Objeción señalada. El propósito de este documento es explorar la noción de OO de Kay, y lo anterior es una de las fuentes verificables que pudimos encontrar, incluso si refleja Smalltalk alrededor de 1974 en lugar de OO como un todo, demuestra sus pensamientos (en un momento, al menos) sobre el asunto.

---

La definición de [AlanKay](https://wiki.c2.com/?AlanKay) de OO es en gran parte la dada por [CarlHewitt](https://wiki.c2.com/?CarlHewitt) para [ActorsModel](https://wiki.c2.com/?ActorsModel), que es un modelo de computación, no un paradigma de programación. Alan Kay ha reconocido explícitamente esta derivación.

Las versiones de Smalltalk anteriores a Smalltalk-80 todavía se basaban en gran medida en el [ActorsModel](https://wiki.c2.com/?ActorsModel) de computación (asincrónico, unidireccional), pero con Smalltalk-80, los desarrolladores de [SmalltalkLanguage](https://wiki.c2.com/?SmalltalkLanguage) cambiaron completamente al modelo de procedimiento (sincrónico, bidireccional), mientras conservaban engañosamente la terminología de [ActorsModel](https://wiki.c2.com/?ActorsModel). (como "mensajes" para lo que esencialmente son llamadas de procedimiento en lugar de notificaciones unidireccionales).

Esto ha causado infinitas dificultades terminológicas, especialmente cuando se considera que las otras fuentes principales del pensamiento orientado a objetos (las arquitecturas de capacidad y la investigación SIMULA 67) no se inspiraron en lo más mínimo en el pensamiento ActorsModel.

---

Entonces, ¿cómo puede afirmarse que lo anterior es [AlanKaysDefinitionOfObjectOriented](https://wiki.c2.com/?AlanKaysDefinitionOfObjectOriented)?

* Estamos tratando de descubrir qué es. Muchos hacen referencia a él y lo citan como la definición canónica. Editaré el texto introductorio para aclarar este punto.

---

Una versión algo modificada de la definición de [Alan Kay](https://wiki.c2.com/?AlanKay) se da en [TimBudds](https://wiki.c2.com/?TimBudd)  [AnIntroductionToObjectOrientedProgramming](https://wiki.c2.com/?AnIntroductionToObjectOrientedProgramming). Curiosamente, la fuente (dada en el texto del libro de Budd) para esta definición es [EarlyHistoryOfSmalltalk](https://wiki.c2.com/?EarlyHistoryOfSmalltalk); aunque esta definición tiene algunas diferencias considerables con la primera. Según Budd:

```
"Alan Kay, considerado por algunos como el padre
de la programación orientada a objetos,
identificó las siguientes características
como fundamentales para OOP:"
```

1. [TodoEsUnObjeto](https://wiki.c2.com/?EverythingIsAnObject).
2. La comunicación es realizada por objetos que se comunican entre sí, solicitando que los objetos realicen acciones. Los objetos se comunican enviando y recibiendo mensajes. Un mensaje es una solicitud de acción, junto con cualquier objeto que pueda ser necesario para completar la tarea.
3. Los objetos tienen su propia memoria, que consiste en otros objetos.
4. Cada objeto es una instancia de una clase. Una clase simplemente representa una agrupación de objetos similares, como números enteros o listas.
5. La clase es el depósito del comportamiento asociado con un objeto. Es decir, todos los objetos que son instancias de la misma clase pueden realizar las mismas acciones.

Hasta ahora, similar a 1-5 arriba. La regla 6 es diferente. Se elimina la referencia a las listas, en su lugar tenemos:

6. Las clases se organizan en una estructura de árbol de una sola raíz, denominada jerarquía de herencia. La memoria y el comportamiento asociados con instancias de una clase están disponibles para cualquier clase asociada con un descendiente en esta estructura de árbol.

---

AlanKay tiene más que decir sobre esto en AlanKayOnMessaging. Si bien no da una definición más nueva en ese mensaje (que es una publicación en una lista de correo, no un escrito académico), parece restar importancia a la construcción de los objetos en sí y, en cambio, se centra en la interfaz entre ellos.

En este sentido, muchas de las reglas enumeradas anteriormente pueden verse como observaciones sobre Smalltalk-80, en lugar de prescripciones/proscripciones que todos los lenguajes OO deberían seguir. De hecho, muchos lenguajes OO modernos e interesantes, incluido [SelfLanguage](https://wiki.c2.com/?SelfLanguage), violan las reglas 4 y 6 de manera rutinaria. [CommonLispObjectSystem](https://wiki.c2.com/?CommonLispObjectSystem) y sus descendientes (DylanLanguage, CecilLanguage), así como otras cosas ([TutorialDee](https://wiki.c2.com/?TutorialDee)), prescinden de la regla 5 y optan por sacar el comportamiento de las clases.

---

Echando leña al fuego, se dice que AlanKay comentó: _"Inventé el término orientado a objetos, y puedo decirles que C ++ no era lo que tenía en mente"_. Ya sea que se opusiera a alguna característica específica u omisión de C++, su calidad o filosofía general, o simplemente participar en una llama gratuita de la "competencia" (Java no existía en ese momento [uh, sí lo hizo, esto estaba en el OOPSLA '98] ), no está claro.

En el artículo ¿Es la ingeniería de software un oxímoron?, Kay escribe: _"Hasta que se desarrolle la ingeniería de software real, la mejor práctica es desarrollar con un sistema dinámico que tenga un enlace extremo en todos los aspectos"_. Si bien esto no limita necesariamente la definición de OO en su mente, es una declaración clave de la filosofía. C++, por supuesto, hace enlaces anticipados en todos los lugares donde puede, hasta el punto de realizar StaticDispatch de forma predeterminada (tiene que solicitar DynamicDispatch con la palabra clave "virtual" cuando lo desee. [e incluso eso, como en muchos otros lenguajes como Java, es solo un envío dinámico único. Si desea un "enlace tardío en todas partes", necesita un sistema de envío mucho más potente, por ejemplo, los genéricos de CommonLispObjectSystem]).

---

Le pregunté a Alan Kay sobre su definición de "orientado a objetos" y me dijo en 2003:

_"OOP para mí significa solo mensajería, retención local y protección y ocultación del proceso de estado, y [LateBinding](late-binding.md) extremo de todas las cosas."_"

Ver http://www.purl.org/stefan_ram/pub/doc_kay_oop_en
