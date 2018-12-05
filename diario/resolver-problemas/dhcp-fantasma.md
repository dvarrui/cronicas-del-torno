
# El servidor DHCP fantasma.

## Entro al aula 109

El martes 4/12/2018 entro en el aula 109. Conecto mi portátil a la red.
Enciendo y entro. Pero... no tengo acceso a internet. Sólo pasa en mi equipo. Todos los alumnos en sus máquinas reales y virtuales tienen la configuración de red correcta.

Primero reviso la configuración de red a ver si es correcta:
`ip a`. Tengo una IP de la red 172.19.0.0 esto es 172.19.99.98 y la máscara también es correcta. OK.

Hago `ping 8.8.4.4` pero no tengo conectividad con el exterior. Oh! ¿qué le pasa a la puerta de enlace? Hago `ip route`  y ... veo que tengo como gateway a `172.19.99.116`... pero ¿por qué? Por eso no tengo salida hacia  a fuera. La puerta de enlace debe ser `172.19.0.1`.

Sospecho que hay un servidor DHCP en la red que me está configurando mal la tarjeta de red.

Como tengo prisa, decido poner la configuración de red en modo estático en mi portatil y... ¡perfecto!.

---

## Entro al aula 108

Al entrar al aula 108 que tiene otra configuración de red, vuelvo a poner la configuración en modo dinámico y mi equipo obtiene una configuración correcta. Todo bien.

Entonces deduzco que el problema está en el aula 109 y debe ser que alguien tenía activo un servidor DHCP que configuraba mal mi equipo.

---

## Conclusiones

Al día siguiente vuelvo al aula 109 y con la configuración dinámica el portátil se configura bien. Ummmmm

Les pregunto a los alumnos que clase tenían el martes antes de mí y qué clases tenían el miércoles antes de mí. Resulta que cuando trabajan en la asignatura de servicios de red han trabajado el servidor DHCP y al llegar yo después han dejado la MV encendidas y con el servidor DHCP activo y mi portátil se ha configurado mal.

Acciones:
* Desinstalen o desactiven el servidor DHCP ¡por dios! ¡Que ya terminaron la práctica!.
* Apaguen las MV de otras asignaturas antes de que yo llegue. ¡Gracias!
