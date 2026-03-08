[<<back](README.md)

# Object Oriented Programming

Programación orientada a objetos

> Enlace al artículo original: https://wiki.c2.com/?ObjectOrientedProgramming

Consultar la definición definitiva en [NygaardClassification](https://wiki.c2.com/?NygaardClassification).

_Nygaard no acuñó el término "Programación orientada a objetos", lo hizo Alan Kay, por lo que no entiendo cómo la clasificación de Nygaard es la "definitiva". ¡Sí!, Simula de Nygaard y Dahl fue el primer lenguaje en tener "objetos", si ignoramos SketchPad del Dr. Ivan Sutherland que es 5 años anterior, pero Nygaard y Dahl no usaron el término OO para describir Simula._

_AlanKay y XeroxLearningResearchGroup tomaron prestadas ideas de muchos lenguajes, incluidos Simula y Lisp, al crear Smalltalk. En Smalltalk, todo es un objeto y cada acción se realiza enviando mensajes a los objetos. Fue por esta razón que Kay describió su lenguaje como "orientado a objetos". Smalltalk fue responsable de popularizar OO como paradigma. Smalltalk es para OO lo que Lisp es para la programación funcional. Hasta el día de hoy, Smalltalk se considera el santo grial de OO; cada lenguaje OO se compara con él. Simula, desafortunadamente, no es más que ALGOL con clases._

_Entonces, si hay una definición de OO definitiva, probablemente deba ser la de Alan Kay. Consulte AlanKaysDefinitionOfObjectOriented y AlanKayOnObjects._

Durante el transcurso de la historia, muchos autores han redefinido el término para que signifique muchas cosas. Veamos algunas de estas definiciones de OO.

Para bien o para mal, es la "calle" en última instancia lo que termina de definir los términos existentes, no los originadores. Por ejemplo, "diezmar" solía referirse a la práctica romana de castigar a los ejércitos matando a uno de cada 10 soldados. Ahora significa destrucción total, no una décima parte. Nygaard puede ser el romano en este caso.

* Una posición inteligente sería alinearse con lo que la calle haya decidido que significa el término. Pero no se puede, porque la calle no lo ha decidido.
* _¿Está sugiriendo que vayamos al origen porque la calle no ha llegado a un consenso?_ Generalmente, los diccionarios tienden a clasificar las diferentes definiciones. Por lo tanto, si se ajusta a las variaciones más populares, entonces es más OO que algo que solo se ajusta a una definición más baja. Hmmmm. _¿Algo que se ajusta a 2 definiciones más bajas se considera mejor que algo que solo se ajusta a la definición superior?_
    * (1) criticar un argumento que argumenta en contra del tema A no es lo mismo que apoyar A (puede o no serlo).
    * (2) Los diccionarios a veces, pero no siempre, dan una idea de cuáles son las definiciones más comunes. Eso NO convierte en menos corresctos al resto.
    * La mayoría de los diccionarios contemporáneos no pretenden decir qué usos son correctos; indican qué usos están o estuvieron en uso.

La "Calle" no decide el significado de los términos. Para eso sirve la comunidad académica (y los diccionarios). De lo contrario, todo el lenguaje humano se disolvería en la ambigüedad, especialmente si hay quienes solo quieren usar términos a la fuerza en el habla para tomar el poder. En cualquier caso, si no hay un buen consenso dentro de las publicaciones de la academia, o si ningún líder está replanteando las definiciones que se usan para y en el campo, entonces debería ir con quien acuña primero.

Ya que estamos hablando de romanos, los plebeyos no escriben historia. Nygaard puede no ser popular entre las grandes masas de personas que juegan con los teclados, pero ciertamente es relevante donde importa. Libros importantes como [SiCp](https://wiki.c2.com/?SiCp) y [TheoryOfObjects](https://wiki.c2.com/?TheoryOfObjects) se suscriben a la definición de Nygaard y, por lo tanto, la generación de estudiantes de élite lo aprenderá. Los libros que popularizan otras cosas para el consumo de la "calle" probablemente sean tragados por el basurero de la historia.

Aunque no es un argumento hermético, me inclino a estar de acuerdo. A diferencia de los dialectos callejeros, la jerga técnica tiende a tener fuentes autorizadas de juicios de corrección, al igual que los problemas técnicos en general. El mal uso de la jerga técnica por parte de las masas constituye un préstamo con un cambio de significado, no un cambio en el significado original. Ejemplo clásico: "salto cuántico" en el lenguaje común no significa lo mismo que en física. Eso no hace que el significado físico sea incorrecto. Permanece intacto.

Pero las masas en este caso no están necesariamente "equivocadas". Las masas no pueden cambiar la física, por lo que hay un punto central para comparar. Hasta ahora, el diseño de software no tiene un núcleo objetivo más que métricas como la velocidad de ejecución y el tamaño del código, que la mayoría está de acuerdo en que son solo una parte de la imagen. Además, algunos "grandes nombres" no están de acuerdo con la definición de Nygaard, no solo las "masas".

Sugiero por tanto [DefinicionesParaOo](https://wiki.c2.com/?DefinitionsForOo).

---

El corazón de OOP es el Refactor [ReplaceConditionalWithPolymorphism](https://wiki.c2.com/?ReplaceConditionalWithPolymorphism).

No creo que esta sea una opinión de concenso. [OoBestFeaturePoll](https://wiki.c2.com/?OoBestFeaturePoll).

Considere un programa procedimental con varias sentencias 'switch', cada una activando lo mismo. Cada bloque 'switch' con la misma lista de declaraciones 'case'.

Puede consultar más del tema en [SwitchStatementsSmell](https://wiki.c2.com/?SwitchStatementsSmell).

---

En inglés, el "objeto" de una oración es el receptor de una acción. Por ejemplo, en la oración "Haga clic en el botón", el "botón" es el objeto.

Desafortunadamente, en programación los "objetos" realizan "acciones". En este sentido, son más afines al "sujeto" de la gramática inglesa.

Correcto. En la gramática inglesa el sujeto realiza la acción. El sujeto puede recibir la acción cuando el verbo es pasivo o intransitivo. Se podría argumentar que un objeto indirecto no recibe una acción, aunque en el esquema completo si la recibe.

ObjectOrientedProgramming se enfoca en "objetos", de modo que lo anterior se puede codificar como: `button.click()`

En cambio ProceduralProgramming  se centra en "verbos", y el código seria como: `click(button)`. Esto implica un cambio ideológico y sintáctico. En lugar de pensar en qué eventos suceden y cómo suceden, pensamos en qué entidades existen y cómo interactúan.

* "click" en este caso no es una acción realizada por botón. Hacer click es lo que otra persona hace para pulsar el botón y, por lo tanto, el botón es realmente el objeto de la oración.
* Lo que parece faltar es el sujeto: la entidad que realiza la acción "click" a la que reacciona el botón. El sujeto casi siempre, de forma implícita, parece ser el objeto que contiene el código, en este caso `button.click()`.

No, es solo un cambio trivial en el azúcar sintáctico. Hay sistemas OO en los que se utiliza la sintaxis de llamada de función normal, p. [CommonLispObjectSystem](https://wiki.c2.com/?CommonLispObjectSystem): (haga clic en el botón). En cualquier sintaxis, está perfectamente claro que el botón es un sustantivo y el clic es un verbo. No hay ilusión de que en button.click(), click sea otra cosa que una función miembro y button sea un objeto.

No es sólo es, es mucho más. En `button.click()`, click puede ser uno de varios métodos, en button, mientras que `click(button)`, click es un método para cualquier botón. La razón por la que los programadores orientados a objetos usan ese ejemplo es que es una buena manera de hacer que los programadores de procedimientos vean la diferencia, ya que la mayoría de nosotros también éramos programadores de procedimientos al principio.

No se trata tanto de la sintaxis como de crear una sintaxis que permita múltiples implementaciones virtuales. Los paradigmas procedimentales no hacen esto, los sistemas de objetos sí, y CLOS es un sistema de objetos. Tiene esas múltiples implementaciones virtuales.

Los principios orientados a objetos son propiedades que emergen de este cambio de enfoque.

Las FAQ sobre objetos (http://www.cyberdyne-object-sys.com/oofaq2/) incluye lo siguiente:

_Simula fue el primer lenguaje con objetos, clases, herencia y escritura dinámica en 1967 (además de su subconjunto AlgolSixty). Fue pensado como un medio de transporte de diseño orientado a objetos._

El lenguaje Simula67 [SimulaLanguage], inventado por OleJohanDahl y KristenNygaard, fue el primer lenguaje de programación orientado a objetos: Simula no inventó el enfoque orientado a objetos, implementó objetos, etc. Los borradores originales llamaban a los objetos 'procesos', pero Dahl decidió usar la palabra "objeto" aproximadamente un año antes del lanzamiento de Simula67 (¡que fue en 1968, por supuesto!). La terminología moderna de clases y herencia estaba toda allí en el lenguaje. El término Objeto posiblemente fue acuñado por Ivan Sutherland antes por algo similar, y el término Orientado a objetos probablemente fue acuñado por Alan Kay (ver AlanKayOnObjects y HeDidntInventTheTerm para una discusión más detallada).

En términos de programación (a diferencia del diseño), un lenguaje OOP generalmente admite lo siguiente:

* Encapsulación
* Herencia (o delegación)
* Polimorfismo

¡¡Advertencia!! ¡¡Advertencia!! Esta definición se considera controvertida en algunos sectores. Por ejemplo, la encapsulación no forma parte de cómo Perl implementa OO; algunas personas pueden querer agregar clases a la mezcla, pero eso excluye los lenguajes basados en prototipos, como SelfLanguage, que definitivamente 'sienten' OO. En particular, las características comúnmente agregadas y eliminadas de esa definición incluyen:

* Identidad de objeto
* Gestión de memoria automatizada (no en CeePlusPlus)
* Clases (¿en qué se diferencia esto de la encapsulación?)
* Tipos de datos abstractos
* Estado mutable

Como mínimo absoluto, la "objetness" representa una combinación de estado y comportamiento. (Atributos/propiedades con métodos. O simplemente ranuras como en Self: la distinción entre atributos y métodos es artificial y algo malo si alguna vez expuso un atributo y desea cambiarlo a un método).

Consulte [Programación basada en prototipos](https://wiki.c2.com/?PrototypeBasedProgramming).

---

**Encapsulación**: (1) los atributos de un objeto se pueden ver o modificar solo llamando a los métodos del objeto; o (2) la implementación del objeto puede cambiar (dentro de límites razonables) sin cambiar la interfaz visible para las personas que llaman.

La segunda es la definición más fuerte, argumentando a favor de minimizar el número de "propiedades" "captador/definidor" exportadas por el objeto, sustituyendo en su lugar "interfaces comerciales lógicas por funcionalidad".

La definción (1) es más restrictiva ya que impone la encapsulación en lugar de recomendarla.

La encapsulación (2) es OOP-universal, se puede decir que es la principal técnica abstracta, lo que diferencia una clase CeePlusPlus y una estructura CeeLanguage.

PythonLanguage y otros rechazan la ocultación de datos (1). Personalmente, no me importa como una herramienta de simplificación siempre que no sea demasiado difícil de romper (RubyLanguage). -- J. Jakes-Schauer

---

**Herencia (o delegación)**: La definición de un objeto amplía/cambia la de otro.

COM y CORBA dirían que este es un problema de implementación y que no es fundamental para el "OO-ness".(Sin embargo, es una característica muy conveniente para la reutilización de código, particularmente en frameworks).

El AdaLanguage, antes de admitir la herencia, se le consideraba un lenguaje basado en objetos. Esta terminología se utilizó para diferenciarlo de los lenguajes orientados a objetos.

Consulte [Programación basada en objetos](https://wiki.c2.com/?ObjectBasedProgramming). --[David McReynolds](https://wiki.c2.com/?DavidMcReynolds)

---

**Polimorfismo**: Capacidad de trabajar con varios tipos diferentes de objetos como si fueran el mismo.

COM, CORBA, Java: Interfaces.

C++: funciones "virtuales". (O "interfaces" con AbstractBaseClass-es y funciones virtuales "puras" (sintaxis "=0").)

¿Esto no se aplica también a los métodos abstractos de Java? [Se aplica a todos los métodos de objetos en Java.]

Smalltalk: Despacho en tiempo de ejecución basado en el nombre del método. (Cualquier dos clases que implementen un conjunto común de nombres de métodos, con "significados" compatibles, son polimórficas. No se necesita una relación de herencia).

:Discusión:

No creo que las interfaces de Java tengan nada que ver con el polimorfismo, y el "Interfaz" en CORBA es sinónimo de "Clase" en otros lenguajes orientados a objetos. Cualquiera de las dos clases que comparten un padre común y proporcionan implementaciones alternativas de un solo método definido en ese padre son "polimórficas". AlanKay describe el estilo polimórfico como "CallByDesire" (a diferencia de CallByValue y CallByName). -- TomStambaugh

_Que no lo crea no significa que no sea así. Las interfaces de Java permiten el polimorfismo puro (independiente de la herencia). También tienen otros usos, y es posible que nunca los use como un mecanismo para incluir polimorfismo en sus diseños, pero el mecanismo está ahí._

Absolutamente adecuado para la mayoría de los lenguajes de implementación OO, como C++. Pero...

En COM y Java, dos objetos cualesquiera que implementen la misma interfaz son (en su mayor parte) "intercambiables": puede usar uno en lugar del otro. COM no tiene herencia de implementación, por lo que "compartir un padre común" (que no sea IUnknown) no tiene sentido (a menos que uno comience a hablar sobre un lenguaje de implementación en particular, como C++). Las clases de Java están limitadas a la herencia única, pero pueden implementar cualquier cantidad de interfaces. Entonces, Java tiende a usar interfaces sobre la herencia de clases para el polimorfismo.

Sí, las "interfaces" de CORBA tienden a significar también "clases". Pero dos servidores CORBA pueden implementar la misma interfaz CORBA para lograr polimorfismo. --JeffGrigg

Las interfaces CORBA admiten polimorfismo, así como las interfaces COM o Java, y las referencias a las interfaces CORBA son igual de "sustituibles". Puede tener tantas implementaciones diferentes de una interfaz CORBA como desee. No creo que las correspondencias uno a uno entre la interfaz y la implementación sean más frecuentes en CORBA que en cualquier otro sistema orientado a objetos. (¿O me estoy perdiendo algo?) -- Kris Johnson

---

Diría que las dos características requeridas de un ObjectOrientedLanguage serían Encapsulación y Polimorfismo. La herencia es solo cómo algunos lenguajes proporcionan polimorfismo. -- JonStrayer

---

Consulte ["¿Es Java orientado a objetos?"](https://wiki.c2.com/?IsJavaObjectOriented) "Irrelevante" Las preguntas de este tipo, y especialmente en una página con el título Programación orientada a objetos, siempre son relevantes. No es "popular" entre algunas personas, pero vale la pena investigarlo considerando el lenguaje que se vaya a usar.

---

Esta discusión exclusivista hace un gran flaco favor a la comunidad OO. Realmente, todo el mundo quiere que OO sea su versión de la historia.

¿Alguien estará de acuerdo en que hay varios modelos OO, teorías? ¿Y alguien se molestará en dar referencias a la teoría OO real en lugar de dar vueltas en círculos con Booch, Rumbaugh y similares?

Y por cierto, la distinción entre button.click() y click(button) es realmente ingenua. "Sintáctico e ideológico", esto alimenta a quienes sostienen que la OO no tiene nada que ver con la Informática, cuando en realidad sólo una parte de la gente de la OO no quiere apartarse de una intuición demasiado simplista sobre lo que creen que debería ser la OO. -- AnónimoCobarde

----

Propongo que la programación está en la mente, y que la programación orientada a objetos es uno de los muchos modelos mentales que ayudan al pensamiento de un programador. Estoy de acuerdo en que las declaraciones dogmáticas sobre lo que es y lo que no es OO son generalmente inútiles. Creo que una discusión más útil intentaría descubrir los diversos conceptos utilizados por los programadores, luego evaluarlos por sus costos y beneficios y cómo interactúan entre sí. Como dije en otra parte, creo que los diversos conceptos se modelan mejor en una escala continua en lugar de un booleano (es/no es OO, bueno/malo, me gusta/no me gusta).

-- Rob Williams

Agregaré mi voto a las declaraciones de Rob. Tan pronto como inventa una etiqueta, en este caso OO, ha creado una iglesia/institución. Eso lleva a disputas territoriales. También conduce a la ideología, la revisión histórica y la negación. No necesito todo ese equipaje, tengo un trabajo que hacer. -- Richard Henderson.

En una escala continua, las declaraciones tienen un tono booleano, es decir: "generalmente inútiles" "los conceptos son mejores". Es difícil evitar el booleano cuando se considera usar/no usar. Por no hablar de las construcciones de programación dentro de la programación orientada a objetos, como If, ifElse, for, do, case y While.

---

Podría ayudar pensar en términos de lo que OO intenta lograr, ¿cuál fue la motivación para desarrollar lenguajes OO? Tal vez eso arroje algo de luz sobre lo que es OO.

Por un lado, estoy de acuerdo en que la programación está en la mente. Debido a que OO está un paso más cerca de la forma en que piensan los humanos (la taxonomía es un buen ejemplo), nos ayuda a diseñar y escribir programas que son más fáciles de entender, **promover la reutilización de código, la cohesión y el desacoplamiento y la protección de datos**.

Si bien las taxonomías jerárquicas pueden modelar la forma en que *algunas* personas piensan (cada cerebro es diferente), no las encuentro muy reflexivas de la forma en que el mundo real cambia con el tiempo. Consulte Límites de jerarquías. Creo que la teoría de conjuntos es un mejor enfoque de clasificación que los árboles en la mayoría de los casos, pero su implementación tiende a conducir a técnicas similares a las de las bases de datos relacionales, lo que nos lleva a la guerra santa de la incompatibilidad psicológica entre objetos y relaciones.

[Saca las jerarquías de tu cerebro, OO no se trata de jerarquías, eso es solo un detalle de implementación para ayudar a organizar el código.]

Estaba respondiendo a la declaración de "taxonomía", NO diciendo que OO tiene que ver con los árboles.

[Pero no es por eso que nos gustan los objetos. OO se trata de modelar el problema con "cosas", "cosas" inteligentes, objetos. Es fácil razonar sobre los objetos, no las clases, sino las instancias de objetos, digamos, por ejemplo, una Persona y una Compañía, es más fácil para la mayoría de las personas razonar sobre ellos imaginando una conversación entre ellos, qué podrían decirse o hacer esos objetos entre sí. ... tal vez unaEmpresa.contrata(unaPersona), o unaEmpresa.despide(unaPersona) o unaPersona.renuncia(unaEmpresa), o preguntas como unaEmpresa.emplea(unaPersona) o unaPersona.trabajaEn(unaEmpresa) o unaEmpresa.esPropiedad(unaPersona) o aPerson.isCompatible(anotherPerson) or aCompany.isOwnedBy(anotherCompany)... or aCompany.employs(anotherCompany)... oops, los últimos dos mensajes se usaron dos veces, pero está bien, el polimofismo elige el método correcto para isOwnedBy dependiendo de si Paso de una empresa o una persona, lo mismo con empleados, un mensaje, pero funciona para varios contextos diferentes, al igual que el lenguaje humano real. Si eso fuera procedimental, tendría que recordar una cantidad mucho mayor de elementos del lenguaje para lograr el mismo trabajo, y tengo que recordar dónde están y cuáles son los conjuntos de registros genéricos que estoy pasando en lugar de objetos, qué módulos incluir.]

* ¿Por qué no modelar esas relaciones con modelos relacionales? Así no habría que leer código voluminoso para ver las relaciones, y se implementaría de manera más consistente de un desarrollador a otro. Y se podría consultar más fácilmente que ese tipo de basura integrada en el código. [No se pueden encapsular enlaces](https://wiki.c2.com/?CantEncapsulateLinks).

_Entonces, ¿por qué no usar un lenguaje de programación declarativo/lógico? Owns(person, company). Owns(company, company). Are-compatible(person1, person2). Es gracioso ver hablar sobre abstracción y polimorfismo mientras se entusiasman con el azúcar sintáctico para los punteros._

OO no es solo sintaxis, también es un enfoque. Es posible implementar principios OO sin usar la sintaxis OO. La sintaxis solo está ahí para fomentar los principios. Para ver un ejemplo de prácticas OO sin sintaxis, consulte http://api.drupal.org/api/file/developer/topics/oop.html/6.

[Solo expliqué por qué.... Owns(person, company) me obliga a recordar que Owns es un comando válido, si hay 300 mensajes en el sistema, debo recordarlos todos, y simplemente no puedo recordar tantos comandos , mientras que aCompany.Owns(aPerson) me obliga a no recordar nada... Simplemente miro una empresa y veo lo que le puede decir a una Persona, o miro a la persona y veo lo que le puede decir a una Empresa. Ese pequeño azúcar sintático lo es todo, proporciona alcance al conjunto de mensajes a los que un objeto puede responder y me quita la carga de recordar esos mensajes. Hay una gran diferencia entre method(arg, arg) y arg.method(arg) en cuanto a lo que la mente debe comprender y recordar. Puede que todo se reduzca a lo mismo, pero a quién le importa, son todos 1 y 0 de todos modos. Pero a nivel de lenguaje hace una gran diferencia en la eliminación de la complejidad de la mente de los programadores.]

Y como ChrisDate, FabianPascal et al. digamos, un DBMS relacional es una herramienta para organizar hechos (es decir, proposiciones declarativas como las anteriores) sobre un dominio. ¿Por qué codificaría a mano su propia versión incompatible y bizantina de dicha herramienta, haciéndola completamente dependiente de una aplicación y arquitectura en particular? (Ciertamente hay razones legítimas, solo me pregunto cuáles son las tuyas).

No soy el mejor, pero puedo oler la publicidad de la industria cuando la veo.

[Con los objetos, uno simplemente recuerda lo que pueden decirse, y si nos olvidamos, sabemos exactamente dónde mirar, ya tenemos objetos en la mano, así que solo míralos. Es literalmente como jugar con legos cuando eras un niño (no estoy seguro si lo hiciste). Una vez que tiene algunas partes básicas en la mano, luego las entidades de la parte de comportamiento del dominio del problema, realmente no pensamos en los datos todavía, eso viene después. Tenemos todos los elementos para construir el programa y resolver cualquier problema a mano, podemos usar los mismos elementos para resolver cualquier cantidad de problemas diferentes sin tener que crear nuevos elementos. Podemos borrar los datos más tarde según lo dicte la necesidad. A medida que el comportamiento se agrega pieza por pieza, agregamos los datos necesarios para respaldar ese comportamiento. Los programas orientados a objetos tienen una organización a nivel de objeto (no clases) que los programas procedimentales no pueden. Los programas procedimentales tienen procedimientos, los programas OO tienen procedimientos sensibles al contexto, el mismo nombre de procedimiento puede tener 15 contextos diferentes en los que puede funcionar, por lo que podemos simplificar nuestro lenguaje de solución. Podríamos hacer lo mismo con el procedimiento al tener un procedimiento grande que tenga los 15 contextos en una declaración de cambio grande. Si bien esto facilita la adición de nuevos procedimientos, hace que sea casi imposible agregar nuevos contextos a grupos de métodos. La solución OO permite agregar contextos completamente nuevos en un abrir y cerrar de ojos, y parece que lo encontramos más importante y más útil. Si la palabra "Contiene" es un mensaje/procedimiento para determinar si una cosa contiene otra, la solución de procedimiento tendría un método Contiene grande y largo que manejaría todos los casos posibles de entrada. La solución OO tendría un método Contiene para todos y cada uno de los contextos diferentes.]

[Las funciones genéricas de lisp, por ejemplo, muy poderosas, muy flexibles y aún así, a menos que sepan y memoricen todas las funciones disponibles, es probable que no sepa que Owns existe. Son indispensables cuando realmente necesita un envío múltiple, pero en la mayoría de los escenarios... un solo envío es todo lo que se necesita y object.method(arg) es simplemente más fácil de razonar. También se pueden consultar qué mensajes responde el objeto. Las funciones genéricas no permiten eso, me obligan ha recordarlo todo. Entonces, en la mayoría de los casos, la programación orientada a mensajes de envío único es más fácil, cuando no lo sea, iremos a la función genérica. En pocas palabras... el objeto proporciona un alcance muy necesario a la lista de mensajes disponibles. Si el mensaje Owns solo funciona con personas y empresas, entonces debe estar en persona o empresa, no vivir solo en un módulo. Me encantan las funciones genéricas, pero no son la respuesta en la mayoría de los escenarios. Tal vez me estoy perdiendo algún concepto fundamental y simplemente nos estamos comunicando mal, no conozco a Haskell, así que no dudes en corregirme si me equivoco.]

_No hay absolutamente ninguna diferencia entre "owns aPerson aCompany" and "aPerson # owns aCompany", es solo sintaxis. De hecho, en Haskell simplemente defino el operador # de tal manera que transforma la segunda forma en la primera. Pero no tiene mucho sentido, no necesito engañarme sobre la "naturalidad" de alguna metodología de diseño. Este debate sobre cómo el operador de acceso de miembros es de alguna manera superior a cualquier otra cosa bajo el sol es simplemente estúpido._

[aPerson.Contains(anAddress) está en un contexto diferente a aCompany.Contains(anAddress), pero usar el contexto de esta manera aprovecha nuestras habilidades sociales y lingüísticas naturales como humanos. Me imagino a los objetos hablando entre sí, luego de repente queda claro cómo una pequeña conversación entre ellos resolve el problema.]

[Puede que no esté de acuerdo, pero la mayoría de la gente está de acuerdo, OO es más natural, somos animales sociales y personificar nuestros objetos nos permite usar esas habilidades sociales innatas para recordar fácilmente cómo interactúa una gran cantidad de objetos, simplemente en función del contexto. El lenguaje se basa en metáforas, abstracciones y contexto, OO proporciona todo esto usando los mismos elementos que el lenguaje hablado usado para describirlo. Nada podría ser más natural que escribir código como anOrder.add(anItem), aCustomer.add(anOrder), aCustomer.add(anAddress), anOrder.add(anAddress), add que se usa en varios contextos diferentes, pero cada uno tiene un implementación completamente diferente, en un método separado. Lo que es más importante, no tengo que recordar que add existe, en un programa de procedimientos tendría que saber acerca de add, en un programa OO solo le pregunto al objeto, si es compatible con add, entonces lo uso. A la mayoría le resulta más fácil mantener muchos procedimientos pequeños y simples que mantener algunos procedimientos gigantes, y los más pequeños son más seguros porque si se estropea uno, no afectará al resto. Estoy seguro de que refutarás todo lo que acabo de decir, pero siempre dices que no entiendes cómo pensamos y por qué nos gusta OO, y te estoy diciendo por qué, no estoy discutiendo, y realmente no Necesito una refutación, solo digo que así es como pensamos. Ha sido explicado suficientes veces por suficientes personas que no creo que puedas decir honestamente que no entiendes cómo pensamos, solo tienes que decir que no estás de acuerdo o que no piensas de esa manera... está bien. ¡Pero así es como pensamos y tienes que entender eso ahora!]

Me parece que OO es una progresión lógica de la programación procedimental. Empecé a programar con Microsoft Professional Development System para BASIC. Después de un tiempo (no mucho, porque me volví un fanático), comencé a diseñar y programar de forma que visto en retrospectiva, estaban orientadas a objetos. Me dió satisfacción poder resumir el código en una abstracción de alto nivel para poder hacer una llamada de procedimiento que dijera 'doThis(instanceData)' y no tener que preocuparme por lo que estaba involucrado en el nivel de tuercas y tornillos. OO también lo hizo posible.

En un lenguaje procedimental, mi doThis(instanceData) puede consistir en varias llamadas a funciones, digamos doThisPart(instanceData); doStillThisOther(instanciaData); y doSomeOtherPart(instanceData). Si quisiera imitar, por así decirlo, la herencia en este lenguaje procedimental, podría escribir un segundo procedimiento de nivel superior, digamos doThis2(instanceData) que consistiera en llamadas, doThis(instanceData); doStillThisOther(instanciaData); etcétera. Un problema es que no tengo funciones virtuales de doThis(instanceData) que pueda anular, aunque podría refinar/dividir más en partes más pequeñas, doThis(instanceData) y hacer llamadas solo a las partes que necesito.

OO nos da herencia en su lugar. ¿Por qué es mejor este enfoque? --Bryan Hoover

Ver [DeltaIsolation](https://wiki.c2.com/?DeltaIsolation) para una discusión sobre "anulaciones" de procedimiento.

---

¿Qué tal el paradigma de la "Programación impulsada por eventos" (control de flujo de rendimiento, solo escribir controladores de eventos, no acaparar el flujo, etc.), en comparación y contraste con la "Programación orientada a objetos"?

p.ej. ¿Los mejores sistemas O-O también tienen un sistema de tiempo de ejecución basado en eventos en su núcleo? y los primeros sistemas basados en eventos (p. ej., Andrew wm original de Gosling en CMU, etc.) estaban limitados por la falta de una buena jerarquía de clases O-O (p. ej., la reescritura de Andrew wm conduce a Andrew BE2, Insets, ATK, mientras tanto en paralelo con MacApp, luego NeXTStep, MFC y Java).

¿Qué es exactamente la programación impulsada por eventos? La única gran diferencia que veo entre EDP procedimental y OO EDP son las diversas formas de encontrar o enviar los diversos eventos. Se puede usar polimorfismo o MultipleDispatch, declaraciones de cambio/caso o incluso búsquedas de tabla/estructura. Cada grupo probablemente defenderá a su favorito.

-- Chris Koenigsberg

---

Principios Generales o Mantra de OO (No todos estarán de acuerdo con todos estos)

* Un onjeto sabe por sí misma cómo manejar las solicitudes que se le dan.
* Los comportamientos comunes se pueden heredar de los padres en lugar de repetirse en cada hijo.
* Los objetos son como un pequeño ser humano al que se le ha asignado un conjunto de responsabilidades.
* Coloque "envoltorios" de comportamiento alrededor del estado o los datos para que el usuario de la clase/objeto no tenga que saber o preocuparse si está mirando el estado o el comportamiento.

---

Attempts at defining [ObjectOrientedProgramming](https://wiki.c2.com/?ObjectOrientedProgramming):

* ObjectsAreDictionaries.
* AclassIsNothingButaCyclicDependency

What is Oo?

* [DefinitionsForOo](https://wiki.c2.com/?DefinitionsForOo)
* OoIsPragmatic.

---
