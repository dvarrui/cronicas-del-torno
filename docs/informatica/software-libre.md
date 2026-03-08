

# El software libre como un feature técnico

## Introducción

Estamos acostumbrado a hablar u oir hablar del software libre... pero en la mayoría de los casos los hacemos o lo hacen desde los siguientes enfoques:

* El SL como licencia de software.
* El SL como aspecto ético.

En este ensayo voy a hablar (escribir) del SL como elemento técnico. No filosófico, ni legalista.

¿Se puede evaluar un software desde el punto de vista técnico e incluir el feature SL dentro de dicho análsis?
Bueno... únicamente si SL fuera un feature técnico pero no lo es!... o si? Sigamos leyendo.

## Antecedentes

Todo esto surgío a consecuencia de una conversación en el grupo GULIC (Gracias Iván por darme tantas buenas ideas ;-)).

La cuestión era sobre analizar desde un punto de vista técnico un software privativo...

Los profesores de FP y de la Universidad estamos acostumbrados a revisar y valorar software contínuamente en las prácticas entregadas por nuestros alumnos. Revisamos, evaluamos y calificamos pero... lo podemos hacer porque tenemos acceso al código fuente. Esto es, necesitamos:
1. Permiso del autor para acceder al código (Esto va implícito en las actividades de clase)
2. Si fuera Open Source también temdríamos acceso al código.

## Evaluar técnicamente software privativo vs libre 

¿Pero qué pasa si no tenemos acceso al código fuente y queremos evaluar/analizar la calidad o la profesionalidad desde un punto de vista técnico de un software privativo del cual no tenemos acceso al código fuente?

La respuesta corta es... NO podemos evaluarlo. Cuando en clase un alumno no entrega un trabajo la nota es NE (No evaluado). Cuando el alumno entrega el trabajo se le evalúa. Entonces sería posible que un software privativo con nota NE pasara de un día para otro a tener un 85% (Suponemos calificaciones entre 0 y 100%). Pues.... SI. Creo que hasta aquí estaremos deacuerdo tod@s... Creo que no he puesto nada subjetivo ni controvertido.

**Regla 1**: Entonces si tengo 2 trabajos o dos aplicaciones: 
1. SL: tendrá una nota entre 0 y 100 y 
2. Privativa: tendrá un NE mientras no tenga acceso al código fuente.

**Hipótesis 1**: A mi juicio (IMHO) NE < nota entre 0-100. Por tanto, por defecto SL > nota que un privativo.

Si tuviéramos acceso al código fuente del software privativo, y pudiéramos evaluarlo, entonces podría tener una nota y se podría comparar Nota[SL] con Nota[Privativo]. Daría un resultado >, < o ==.

Pero aunque se pudiera hacer lo anterior surge otro inconveniente... una vez tenemos el ejecutable del privativo pierde la nota... y vuelve a ser NE... porque NO tenemos garantía de que el ejecutable privativo provenga del código fuente privativo que evaluamos en el paso anterior. Por tanto el ejecutable volvería nuevamente a NE.

## Evaluar el API 

En un software privativo donde no tenemos acceso al código fuente... sólo podemos evaluar el API. Esto es, la parte exterior o las funciones que parece que nos ofrecen a los usuarios.

Esta forma de evaluar me parece bien que la hagan usuarios normales, pero nosotros lo profesionales NO nos podemos quedar ahí. Me explico con un ejemplo. 

Supongamos que somos cocineros profesionales y queremos evaluar un plato de comida. Lo probamos, nos gusta y ponemos la nota. mmmm eso es la mitad de la evaluación. El sabor la presentación etc son 50% importantes (como el API del software) pero luego necesitamos saber más para evaluar el otro 50%: 
* Ingredientes utilizados.
* Coste de realización de la comida.
* Habilidades/técnicas empleadas con el cocinero.
* Tiempo que se tarda.
* Vamos... que necesitamos la receta.

Si con este ejemplo no queda tan claro como me queda a mí... pues habla conmigo a ver cómo lo puedo explicar mejor.

## Privativo Open Source

Hay un excepción. Si el software privativo fuera además Open Source, entonces SI se le puede poner nota al código fuente y se podría verificar que el ejecutable corresponde conel código evaluado.

A partir de aquí se podría comparar de forma técnica software libre vs privativo.

```
Invitado: Uff... que rollo! No? No rollo... qué cansado! 
          Pero ahora creo que lo veo más claro. IMHO
no-goto-san: :-)
```

## Software libre como feature técnica

```
invitado: Seguimos... ¿más? 
no-goto-san: Si hay que rematar lo último.
```

Las licencias de software (SL también) implican limites o restricciones que tiene el usuario para usar el software.
De la misma forma que si hacemos un programa sin entorno gráfico el programado está restringiendo su uso al terminal, o si un programador hace un programa para la plataforma X está restringiendo su uso para es plataforma únicamente. Programar es dar funciones y restringir. 

**Regla 2**: 
El programa:
* Lo hace el programador para el uso del usuario.
* Impone restricciones al usuario.
* Da algunas funciones de "poder" al usuario.

Dicho de otra forma, el programador decide qué restringe y que poder da al usuario a través de la "magia de su hechizo" (El programa).

**Regla 3**:
Una licencia:
* La pone en autor/propietario del software a su creación.
* Impone restricciones al usuario.
* Da algunas funciones de "poder" al usuario.

Dicho de otra forma, el autor/propietario decide qué restringe y que poder da al usuario a través de la "magia de su hechizo" (El programa).

```
no-goto-san: La similitud entre las definiones anteriores es evidente.
invitado: Ya pero... no es de esa valoración técnica de la que yo quería hablar la verdad.
no-goto-san: No especificaste...
             Existe la valoración técnica aplicada a las técnicas de la informática pura.
             Existe la valoración técnica aplicada a las técnicas de la "jurisprudencia/legalidad" pura.
```

En un software (como en cualquier obra creada por los humanos en esta sociedad actual) confluyen dos elementos:
* Aspectos informáticos.
* Aspectos legales.
* (Incluso se me ocurren algunos más pero... eso es para otro ensayo. Sorry!)

Una valoración técnica generalista lo incluye a todos IMHO.

**Hipótesis 2:** Cuando un autor establece una licencia sobre su obra está definiendo cómo va a "funcionar" su obra en el mundo real con los usuarios.

## Mi opinión personal

Voy a escribir algo que es sólo mi opinión personal (Palabra de Crasidea).

¿Por qué pienso que el SL es superior al privativo desde un aspecto "técnico"?
NO informático NO legalista NO ético NO filosófico.

```
Invitado: Si! ¿por qué? Dilo ya! pesado
```

¿Por qué defiendo SL sobre cualquier privativo?

```
no-goto-san: Mi hermano (es un crack de la informática y muy profesional)
             Mi hermano me dice que soy un intolerante, un intransigente por todo esto.
             yo le digo que lo entiendo pero que yo le veo a él como "un ciego".
             ¡Lo siento!
```

Lo defiendo porque como programador (y usuario de software) NO quiero dañar al usuario.

```
invitado: Qué exagerado! ¿cómo va a dañar al usuario una licencia privativa?
```

Yo lo he vivido ya muchas veces. Y no quiero volver a sufrir.

Antes de mi "desintoxicación" allá por el 2005. usaba un software privativo que me encantaba por su API externa. por la funcionalidad que ofrecía a mí como usuario. Se volvió un software de uso habitual... me enganché. Le dediqué horas y horas de estudio de los manuales, adquirí destreza un su manejo... era feliz. Pero era una falsa relación.

Los propietarios decidieron acabar con el software y se terminó. Pero ¿y ahora yo qué hago?...

Sufrir. Si hubieran liberado el código (SL) podría haber seguido siendo feliz... no ahora me doy cuenta de que el privativo te genera una adicción que cuando desaparece la "droga" es muy difícil y duro de llevar.

**Regla nº 4**: Quiero ser profesional. Soy un profesional.
Pues como tal, y por todo lo anterior... sólo puedo concluir que hay que evitar al 100% el uso de software privativo al usuario. Y no es una cuestión ética no filosófica. Es ser un buen profesional y ser un buen profesional es una cuestión técnica.

¡Muchas gracias por leerme!
(Palabla de no-goto-san)
