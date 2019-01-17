
# Ruby: ¿IDE? ¡No, gracias!

> **WARNING**: Sólo para programadores Ruby o Python. Abstenerse tipados estáticos.

## IDE: Características

Ejemplos de IDE serían:
* Anjuta (C y C++ para GNOME)
* Eclipse
* NetBeans
* SharpDevelop
* Lazarus
* Borland C, Turbo C, etc.

IDE son las siglas de Entorno de desarrollo integrado. Y normalmente, un IDE consiste de:

| ID | Herramienta |
| -- | ----------- |
|  1 | Un editor de código fuente |
|  2 | Un compilador o un intérprete |
|  3 | Un navegador de clases, un buscador de objetos y un diagrama de jerarquía de clases |
|  4 | Un depurador |
|  5 | Un sistema controlador de versiones |
|  6 | Herramientas de construcción automáticas |
|  7 | Auto-completado inteligente de código (IntelliSense) |

---

# Ruby: ¿Por qué no IDE?

```
I: ¿Por qué motivo no vamos a usar un IDE?

R: No lo vamos a usar porque
no nos va a ayudar.
¡Nos van a molestar!.

Los IDE's son pesados,
lentos,
cargan la memoria y
fracamente...
con Ruby NO los necesitamos.
Ya tenemos todo lo que nos hace falta.

I:  Si no vamos a usar un IDE...
¿entonces cómo vamos a poder trabajar?

R: Ahora lo cuento. Vamos a usar herramientas de forma más rápida y ligera.
```

---

# Ruby: Herramientas

| Característica | Herramienta |
| ------------- | ----------- |
| 1 | **Atom** u otro editor de texto plano que reconozca la sintaxis. Ligero y que no nos haga esperar. |
| 2 | Ruby no es compilado. Ya tiene un intérprete. El propio **ruby** lo es. |
| 3 | Tienes documentación web, el comando **ri** da esa información, y también puedes hacer uso de la reflexión y preguntar a los objetos y clases qué es lo que tienen en cada momento. |
| 4 | Tienes el depurador **pry-byebug** que puedes usar de forma integrada en el propio ruby. O puedes usar otros como **pry**. |
| 5 | **Git**. ¡No reinventemos la rueda!  Además podemos usar Git dentro de Atom si queremos. |
| 6 | El **lenguaje ruby es muy expresivo** y no requiere de herramientas de construcción externas. El se construye sólo así mismo.|
| 7 | El lenguaje ruby tiene **metaprogramación y tipado dinámico**. El análisis del código estático nunca puede saber qué métodos tendrá una clase u objeto cuando el programa se ejecute. Todo puede autoprogramarse y cambiar durante la ejecución. ¡No te asustes! Hay formas de tener toda esta potencia controlada (Unit Test) |
