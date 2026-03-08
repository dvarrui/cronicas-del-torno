[<<back](README.md)

# Late binding (Enlace tardío)

> Enlace al artículo original: https://wiki.c2.com/?LateBinding

"Late binding" es cuando las llamadas polimórficas, o cualquier otra operación de enlace, no se resuelve hasta el tiempo de ejecución. Similar, si no idéntico, a [DynamicBinding](https://wiki.c2.com/?DynamicBinding).

¿Se puede decir que LateBinding es lo mismo que [WeaklyTyped](https://wiki.c2.com/?WeaklyTyped) y [EarlyBinding](https://wiki.c2.com/?EarlyBinding) es lo mismo que [StronglyTyped](https://wiki.c2.com/?StronglyTyped)?

No. "Forth" es "weakly typed"; no distingue entre una variable que es un puntero y un número entero. Sin embargo, utiliza EarlyBinding; si al final trata la variable como un puntero o un entero se sabrá en tiempo de compilación.

Tal y como lo veo, WeaklyTyped y StronglyTyped dan idea de los duro que trabaja el compilador para asegurarse de que no existan errores de tipo, mientras que EarlyBinding y LateBinding dicen cuándo funciona.

La tipificación "débil" y "fuerte" se define de manera bastante nebulosa, como los lenguajes de programación de "bajo nivel" y "alto nivel". -- Simon Heath

Consulte [TypingQuadrant](https://wiki.c2.com/?TypingQuadrant) y [LateVsEarlyBinding](https://wiki.c2.com/?LateVsEarlyBinding) para obtener más información sobre esta distinción. Última edición, 25 de enero de 2006
