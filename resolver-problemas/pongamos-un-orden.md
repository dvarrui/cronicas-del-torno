
# Pongamos un Orden

# La historia tiene un orden

Ayer, mi prima nos hizo una sesión de fotos, y hoy, quedamos para ver los resultados. Mi prima es una fotógrafa muy buena (http://www.anabelvargas.com/), y por tanto estábamos muy ilusionados por ver los resultados.

Mi prima hizo fotos, hizo su _magia_ y para terminar _creó una historia_ mediante una secuencia de fotos elegidas que grabó en un pendrive. Para mantener la secuencia de las fotos hizo algo como:

```
Anabel & David Navidades 2018 1.jpg
Anabel & David Navidades 2018 2.jpg
Anabel & David Navidades 2018 3.jpg
etc.
```

Vamos, lo normal. Para que las fotos se vieran mejor decidimos poner el pendrive en la televisión. Seleccionamos dispositivo -> Ver Fotos y ...

> ¡NO! Ese no es el orden que debían tener las fotos.

Aparecen los nombres cortados como:
```
Anabel...
Anabel...
Anabel...
```
> ¡Vaya! Parece que los nombres son demasiado largos para mostrarlos por completo. Y las fotos no aparecen ordenadas como estaban en el MAC...¿por qué?

---

# Dudamos de nosotros mismos

* Comprobamos que en el MAC, el pendrive muestra los ficheros de las fotos de forma ordenada => OK.
* Sospechamos que tiene que ver con los nombres largos y que el SmartTV los muestra de forma acortada. Lo que define la secuencia de orden es la numeración y ésta aparece al final del nombre...

> ¡quiźas! El SmartTV no están Smart como pensábamos

* Decidimos renombrar los archivos de la siguiente forma:

```
01-davidyaaron.jpg
02-davidyaaron.jpg
03-davidyaaron.jpg
etc.
```

> Pero nos encontramos con el problema de que tenemos prisa por ver las fotos y que son... 46. Esto a mano, no lo vamos a hacer.

* Primero buscamos en el MAC la forma de hacer un renombrado masivo de los archivos de forma que cambie la posición de la numeración al principio... no lo encontramos o no lo sabemos hacer.

> A mi no me da vergüenza reconocerlo. ¡Nunca había tocado un MAC!

* Entonces se me ocurre una idea...

---

# Rescate terminal

> Vamos a ver, que yo llevo muchos años trabajando con el terminal. Además los actuales MacOS heredan de los sistemas BSD, y éstos a su vez de los UNIX...¡bien! Igual me sé los comandos...¡probemos!

* Abro un terminal.
* Funcionan los comandos: whoami, pwd, cd, ls, echo, mv, whereis, vi => OK
* Además tenemos Bash. Entonces comienzo a hacer un script Bash para renombrar de forma masiva y automática los archivos de las fotos.

> ¡Eh! Ahora si que soy un devops...automatizar, automatizar.

* Me pongo un poco frustrado porque las combinaciones de teclas en un MAC son diferentes y voy más lento de lo que quería.

> NO estoy contento y pienso...¿cómo podría estar mas feliz?

* Voy al terminal y pongo `ruby -v`.

> ¡EUREKA! Parece que viene instalado por defecto. Vale ya había empezado mi script en Bash y ahora lo cambio a Ruby porque eso me hace feliz. Y es lo que necesito ahora.

* Hago el script en Ruby (La felicidad me hace coger velocidad y caldiad de vida). Éste es el resultado:

```
#!/usr/bin/ruby

number=0
cmd = `ls *.jpg`
files = cmd.split("\n")

files.each do |oldname|
  number+=1

  # Defino el nuevo nombre
  prefix = number.to_s
  prefix = "0#{number.to_s}" if number<10
  newname ="#{prefix}-davidyaaron.jpg"

  # Ejecuto el comando de renombrado
  cmd = "mv \"#{oldname}\" #{newname}"
  puts cmd
  system(cmd)
end
```

* Lanzo el script y hacemos el renombrado masivo.

> Huelga decir... que los script nunca salen a la primera... hay que ir arreglando bugs... pero eso no es relevante para nuestra pequeña historia.

* Vamos al SmartTV, ponemos el pendrive y...

> Las fotos siguen desordenadas a pesar de que nos aseguramos de poner correctamente lo nombres.
>
> ¡Nos frustramos! Pero decidimos ver las fotos ya. Aunque no tuvieran el orden esperado. :-(
>
> ¡Por cierto! Las fotos ¡guapísimas! Mi prima es una crack de la fotografía. Si no lo creen... compruébenlo ustedes mismos.

---

# Las cosas no salen siempre como esperamos

> ¿Pero qué está pasando? Lo habitual es que los exploradores de archivos muestren los ficheros por el orden de sus nombres de archivos. Este caso no.
>
> Entonces ¿qué criterio de ordenación sigue el SmartTV? Ummmm
>
> Alguna información de los metadatos de los archivos debe ser la que se está utilizando como criterio de ordenación... pero ¿cuál? ¡Hay que investigar!

Al llegar a casa, empecé a escribir este caso de resolución de problemas:
* Hablando con mi primo Miguel se nos ocurrió que quizás la fecha de modificación de las fotos podría ser el criterio elegido.
* Este valor aparece en los metadatos.
* Además mi prima Anabel habitualmente cambia los metadatos de forma masiva de todas las fotos que entrega... pero esta vez no lo hizo.
* Entonces decido modificar el script para que haga un renombrado y además cambie la fecha de modificación de los archivos según la secuencia que queremos. Veamos script:

```
#!/usr/bin/ruby

number=0
cmd = `ls *.jpg`
files = cmd.split("\n")

files.each do |oldname|
  number+=1

  # Defino el nuevo nombre
  prefix = number.to_s
  prefix = "0#{number.to_s}" if number<10
  newname ="#{prefix}-davidyaaron.jpg"

  # Ejecuto el comando de renombrado
  cmd = "mv \"#{oldname}\" #{newname}"
  puts cmd
  system(cmd)
  system("touch #{newname}")
end
```

* El resultado tiene buena pinta.

```
alta> ls -l
total 122944
-rw-r--r-- 1 david users 3709555 dic 25 21:14 01-davidyaaron.jpg
-rw-r--r-- 1 david users 4832359 dic 25 21:14 02-davidyaaron.jpg
-rw-r--r-- 1 david users 5188701 dic 25 21:14 03-davidyaaron.jpg
-rw-r--r-- 1 david users 5136536 dic 25 21:14 04-davidyaaron.jpg
-rw-r--r-- 1 david users 3270125 dic 25 21:14 05-davidyaaron.jpg
-rw-r--r-- 1 david users 4419980 dic 25 21:14 06-davidyaaron.jpg
...
(Así hasta 46)
```

* ¿Funcionará?
