
# El servidor DHCP fantasma.

## Entro al aula 109

El martes 4/12/2018 entro en el aula 109. Conecto mi portátil a la red.
Enciendo y entro. Pero... no tengo acceso a internet. Sólo pasa en mi equipo. Todos los alumnos en sus máquinas reales y virtuales tienen la configuración de red correcta.

Primero reviso la configuración de red a ver si es correcta:
`ip a`. Tengo una IP de la red 172.19.0.0 esto es 172.19.99.98 y la máscara también es correcta. OK.

```
david@camaleon:~> ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 50:b7:c3:06:e2:d1 brd ff:ff:ff:ff:ff:ff
    inet 172.19.99.98/16 brd 172.18.255.255 scope global enp2s0
       valid_lft forever preferred_lft forever
    inet6 fe80::52b7:c3ff:fe06:e2d1/64 scope link
       valid_lft forever preferred_lft forever
david@camaleon:~> 
```

Hago `ping 8.8.4.4` pero no tengo conectividad con el exterior. Oh! ¿qué le pasa a la puerta de enlace? Hago `ip route`  y ... veo que tengo como gateway a `172.19.99.116`... pero ¿por qué? Por eso no tengo salida hacia  a fuera. La puerta de enlace debe ser `172.19.0.1`.

```
david@camaleon:~> ip route
default via 172.19.99.116 dev enp2s0 proto dhcp
172.19.0.0/16 dev enp2s0 proto kernel scope link src 172.19.99.98
david@camaleon:~>
```

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
