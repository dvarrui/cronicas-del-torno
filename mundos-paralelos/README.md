
# Mundos paralelos

No se me ocurrió otro nombre mejor (por el momento). En los "mundos paralelos" coexistimos al mismo tiempo pero en realizades diferentes, lo cual genera desconcierto cuando queremos hacernos entender con seres de "otra realidad".

Voy a describir el mio.

# Informática

* La **informática** (computación) se encarga de estudiar los métodos, técnicas y procesos con el fin de almacenar, procesar y transmitir información y datos en formato digital.
* **Información:** conjunto organizado de datos que constituyen un mensaje que cambia el estado de conocimiento del sujeto o sistema que recibe dicho mensaje. 
* **Un dato** es una representación simbólica (numérica, alfabética, algorítmica, espacial, etc.) de un atributo o variable cuantitativa o cualitativa. Los datos representan la información que el programador manipula en la construcción de una solución o en el desarrollo de un algoritmo.
* **Algoritmo** es un conjunto de instrucciones o reglas definidas y no-ambiguas, ordenadas y finitas que permite, típicamente, solucionar un problema, realizar un cómputo, procesar datos y llevar a cabo otras tareas o actividades. Dado un estado inicial y una entrada, siguiendo los pasos sucesivos se llega a un estado final y se obtiene una solución. Los algoritmos son el objeto de estudio de la algoritmia.

# Lenguages de programación

# Variable

Una variable es una referencia que apunta a una dirección de memoria en la que está almacenado un dato (valor). 
La variable puede cambiar la dirección de memoria a la que apunta para reflejar un cambio de contenido.

Ejemplo:

```ruby
episodio = 4
nombre = "Obiwan"
```

La memoria contendría algo como lo siguiente:

| Variable | Posición de memoria | Contenido | Dato | Representa |
| -------- | ------------------: | --------- | ---: | ---------- |
| episodio | 0000 0000           | 0000 0100 | 4    | 4          |
| nombre   | 0000 0001           | 0100 1111 | 79   | O          |
|          | 0000 0010           | 0110 0010 | 98   | b          |
|          | 0000 0011           | 0110 1001 | 105  | i          |
|          | 0000 0100           | 0111 0111 | 119  | w          |
|          | 0000 0101           | 0110 0001 | 97   | a          |
|          | 0000 0110           | 0110 1110 | 110  | n          |

Para cambiar el contenido de una variable

```ruby
episodio = 5
nombre = "Obi-wan"
```

Puede hacerse de dos modos:
* **Datos mutables**: Cambiando el dato de la posición de memoria apuntada por la variable (`episodio`)
* **Datos inmutables**: Escribiendo los nuevos datos en una nueva posición de memoria y cambiando la dirección de memoria a la que apunta la variable (`nombre`).

| Variable | Posición de memoria | Contenido | Dato | Representa |
| -------- | ------------------: | --------- | ---: | ---------- |
| episodio | 0000 0000           | 0000 0100 | 5    | 5          |
|          | 0000 0001           | 0100 1111 | 79   | O          |
|          | 0000 0010           | 0110 0010 | 98   | b          |
|          | 0000 0011           | 0110 1001 | 105  | i          |
|          | 0000 0100           | 0111 0111 | 119  | w          |
|          | 0000 0101           | 0110 0001 | 97   | a          |
|          | 0000 0110           | 0110 1110 | 110  | n          |
|          | 0000 0111           |           |      |            |
| nombre   | 0000 1000           | 0100 1111 | 79   | O          |
|          | 0000 1001           | 0110 0010 | 98   | b          |
|          | 0000 1010           | 0110 1001 | 105  | i          |
|          | 0000 1011           | 0010 1101 | 45   | -          |
|          | 0000 1100           | 0111 0111 | 119  | w          |
|          | 0000 1101           | 0110 0001 | 97   | a          |
|          | 0000 1110           | 0110 1110 | 110  | n          |

Hay lenguajes de programación que están implementados usando:
* Sólo datos mutables
* Sólo datos inmutables
* Mezclando datos mutables e inmutables.

