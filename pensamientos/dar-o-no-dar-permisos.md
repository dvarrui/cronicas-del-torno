
# Dar o no dar permisos

**Analizar la situación**

Como informático, nos encontraremos muchas veces con un usuario que nos hace una petición/solicitud o nos pregunta cómo lo podemos ayudar con su problema. Evidentemente, el usuario nos pregunta por que "siente" que tiene un problema "informático" y por esa razón consulta al experto. Es normal, los usuarios no tienen por qué saber. Para eso estamos los profesionales.

Entonces nos reunimos con el usuario, le preguntamos sobre su problema y qué quiere conseguir, a dónde quiere llegar. No es buena idea que el usuario nos diga cómo tenemos que resolverle su problema. ¡No! El usuario que nos diga a dónde hay que llegar,y ya nosotros decidiremos cuál será el camino que habrá que recorrer.

Como resultado del análisis del problema del usuario, al final llegaremos a conclusiones, nos reuniremos con el usuario y le plantearemos las opciones disponibles, sus pros y contras. En algunos casos, puede incluso, que tras analizar la necesidad del usuario, le tengamos que decir que no se puede hacer por:
1. Cuestiones técnicas: _tecnológicamente no es viable_.
2. Cuestiones sociales: _error de planteamiento del problema original_. Vamos que va a empeorar el problema con otro diferente que no se había planteado.

El caso 2... podría plantear dudas al profesional de ¿lo hago o no lo hago? Sabes que no es correcto, pero claro ¿si el cliente me paga un "pastón"?

Si decides hacerlo, aunque seas consciente de que lo vas a empeorar todo... por favor, que el cliente te lo ponga por escrito y firmado. Y deja de leer este documento aquí y ahora.

---

**Cuestionando el planteamiento**

Si estás leyendo esto, es porque has decidido ser un buen profesional (y no estás apurado económicamente), y le dices al usuario que eso que él pide, no se puede hacer de esa forma porque genera un problema peor.

Cuando un usuario crea archivos en su PC. Estos, por defecto, se crean de su propiedad. Los sistemas de ficheros de los sistemas operativos tienen prohibido que un usuario pueda cambiar el propietario de un archivo. ¿Se podría hacer tecnológicamente? ¡Sí! Pero no se hace... ¿por qué? Porque entonces todo el sistema de ficheros perdería sentido. Ejemplo: Un usuario UA hace un archivo con un contenido (CA) determinado. El usuario UA es responsable de dicho escrito, pero si por un casual le cambia el propietario para el usuario UB... entonces según el sistema de ficheros ¿ahora el responsable es el usuario UB? No tiene sentido. La utilidad de identificar quién ha hecho qué (responsabilidad)... desaparecería?

De forma similar si los sistemas de ficheros permitieran que el usuario UA creara el archivo CA, y que el usuario UA le diera permisos al usuario UB para que pudiera "cambiar los permisos" de CA... nos encontraríamos en una situación similar a la anterior.

**Responsable único**

Podríamos pensar, que si el usuario UA crear el archivo CA y da permisos de lectura y escritura a su grupo GA... entonces todos los miembros del grupo GA podrían modificar el contenido del archivo CA y el usuario UA sería responsable aunque no lo hay escrito...¡Sí! ¡Sí! y ¡Sí! El usuario UA como propietario del archivo CA tiene la responsabilidad sobre CA. Si no quiere asumir responsabilidades sobre CA... no des permisos de escritura a nadie.

No es un problema técnico. Es una cuestión de organización y gestión de la responsabilidad. Es un tema organizativo.

Esto quiere decir que ¿no podemos hacer trabajos colaborativos porque entonces UA es siempre el responsable de todo? No. Para los trabajos colaborativos de este tipo existen las herramientas de control de versiones, por ejemplo Git que pueden hacer un seguimiento de quién ha escrito qué y cuándo.

_Los permisos de los sistemas de ficheros limitan sus funciones para ser óptimos resolviendo el problema que tienen que resolver. NO para hacer todo lo que se le ocurre al usuario._

---

# Permisos rwx

Los sistemas de ficheros XFS, BTRFS, EXT4, etc. Implementan un sistema de seguridad de tres niveles con tres permisos. Estos son:
* Niveles: propietario, grupo propietario, todos.
* Permisos: lectura, escritura, ejecución/navegación.

Si por algún casual quisiéramos asignar permisos donde tuviéramos más de 3 niveles... "rwx" no podría hacerlo tecnológicamente. Debemos pasar a la función de ACL (Access Control List). Por ejemplo, el sistema de ficheros NTFS implementa por defecto ACL. En ACL podemos superar ampliamente la barrera de los 3 niveles de asignación de permisos de los "rwx".

Pero, si aún así, queremos tener ACL en XFS, BTRFS o EXT4 ¡podemos! No viene por defecto, pero si lo quieres lo puedes tener.

---

# ACL vs rwx

¿Entonces si ACL tiene mayores capacidades que rwx podríamos pensar que es superior y por tanto rwx debería ser sustituido por ACL por defecto?...¡No!

El tema es que la seguridad y la asignación de permisos es algo muy importante en los sistemas. Un fallo, puede ser letal. Por tanto no es tan importante que los sistemas de asignación de permisos tengan más funciones sino que las funciones que realicen las hagan bien y que sea sencillo y claro para el usuario. A veces hay que sacrificar funcionalidades en pos de la sencillez de uso que da seguridad en su revisión por parte de los humanos que lo deben supervisar.

ACL permite al usuario complicar mucho las asignaciones de permisos o las denegaciones... y si no queremos que el usuario lo pueda complicar, aunque se empeñe... entonces (en mi opinión) mejor no permitirlo.

---

# Necesidad de ACL

¡Si, ya! Pero resulta que viene un cliente con la siguiente petición.
* Tengo unos archivos CA del usuario UA.
* Todo el grupo GA tiene permisos de lectura y escritura sobre CA (¡Ay! ¡UA vigila!)
* Todos o el resto no tienen permisos.
* Pero se quiere que además el grupo GB tenga permisos de lectura.

Bueno, evidentemente tenemos un problema con asignación de permisos de 4 niveles y rwx sólo resuelve casos de 3 niveles. Tenemos dos opciones:
1. Pasamos de "rwx" a ACL para tener más niveles de asignación y resolver el problema como nos lo pide al cliente.
2. Mantenemos el sistem "rwx" y le damos otra solución al cliente.

Con el punto 2, el usuario puede que se queje. Pero a mi me gusta mucho más ese camino... porque para mí, por encima de lo que pueda pedir el cliente, está mi criterio como profesional de cómo y cuál es el camino correcto. Y para mi lo correcto es primar la seguridad, claridad y sencillez en las reglas de seguridad y permisos.

```
ASEGURAR LA INTEGRIDAD DEL SISTEMA
debe ser mi prioridad como Sysadmin...
porque es mi responsabilidad.
```

;-)
