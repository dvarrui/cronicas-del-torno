[<<back](README.md)

# Tipos de datos

Para empezar ¿Qué es un tipo (de datos)?... bueno, vimos que las variables referencian posiciones de memoria donde se guardan datos, como por ejemplo: 0110 0001. También vimos que la informática va de trabajar con datos, y los datos en los PCs actuales son eso. Ceros y unos.

Como los datos para los humanos no significan nada, entonces asociamos datos a representaciones o símbolos de modo que ya los humanos asociamos significado a esos símbolos.. Entonces el dato anterior ¿qué significa?

* Puede representar el integer 97 si entendemos que el datos es un número binario clásico.
* Puede representar el char 'a' según el encoding UTF-8
* Puede representar ... muchas cosas diferentes. Todo depende del "tipo" de datos que asumamos a ese valor.

Por tanto, los datos a valores no significan nada para los humanos a menos que los asociemos a un determinado "tipo".

## Declaración de tipos

Hay diversas formas de asociar un dato con su tipo:

* Declaración de tipos. Por ejemplo en el "tipado estático", "anotaciones" o en el "gradual typing". Ejemplo
```c
// Declaración
int episodio;
char letra;

// Uso de la variable
episodio = 9;
```

* Sin declarar el tipo de forma explícita. Por ejemplo en el "tipado dinámico" o también en "inferencia de tipos". Ejemplo
```ruby
# Se asume que 4 es un Integer y entonces la variable es ahora de tipo Integer
episodio = 4
```

```rust
// La variable i se declara de tipo i8 pero la variable j se infiere
let i: i8 = 16
j = i;
```

## Asociar variable con un tipo determinado

Para poder manipular los datos de las variables necesitamos saber cómo interpretarlos, esto es, necesitamos tener un tipo asociado.

El momento de realizar esa asociación, o la forma de realizar la asociación determina el modelo de tipado que tiene cada lenguaje de programación. Por ejemplo:

| Tipado   | Momento | Responsable |
| -------- | ------- | ----------- |
| Estático | Los tipos de las variables se establecen antes de poder ejecutar el programa | Es el programado el que de forma explícita define las asociaciones de variable con su tipo. A esto se le llama declaración de variables |
| Inferencia | Los tipos de las variables se establecen antes de poder ejecutar el programa | Es la herramienta compilador/intérprete el encargado de deducir o averiguar el tipo de cada una |
| Dinámico | Los tipos de las variables se establecen durante la ejecución del programa | Es el compilador/intérprete el encargado de deducir o averiguar el tipo de cada una |
| Gradual | Es una mezcla de los anteriores | Es una mezcla de los anteriores |
