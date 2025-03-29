# VOLÚMENES

[← Regresar a notas](../../README.md) <br>

----

Un volumen de Docker es un mecanismo de almacenamiento persistente asociado a los contenedores para conservar y compartir datos de forma independiente a su ciclo de vida. 
Esto permite que los datos se mantengan intactos incluso cuando los contenedores se actualizan o eliminan.

Conoce más: <https://youtu.be/GwnDA-oXShI>

> ### ▶️ Mostrar los volúmenes
> ```shell script
> docker volume ls
> ```
---

> ### ▶️ Eliminar un volumen
> ```shell script
> docker volume rm <volume-id>
> ```
---

> ### ▶️ Eliminar todos los volúmenes
> ```shell script
> docker volume prune
> ```
---