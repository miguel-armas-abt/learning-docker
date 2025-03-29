# DOCKER SWARM

[← Regresar a notas](../../README.md) <br>

----

Docker Swarm es la solución nativa para orquestar contenedores en un clúster distribuido, facilitando la escalabilidad, el balanceo de carga y la alta disponibilidad. A diferencia de Docker Compose, que define y ejecuta aplicaciones en un único host, Swarm se orienta a entornos multi-nodo para producción.

---

## Stack
Un stack representa un conjunto de configuraciones que definen cómo ejecutar un grupo de contenedores de Docker.

---

📌 Utilice `-c` opcionalmente para especificar el archivo yml

> ### ▶️ Activar Docker Swarm 
> ```shell script
> docker swarm init
> ```
---

> ### ▶️ Desconectar nodo del clúster de Docker Swarm (Desactivar)
> ```shell script
> docker swarm leave --force
> ```
---

> ### ▶️ Iniciar los stacks definidos en la orquestación
> - Para iniciar un stack específico podemos agregar su nombre al final del comando
> ```shell script
> docker stack deploy -c <yml-file>
> ```
---

> ### ▶️ Mostrar todos los servicios desplegados
> ```shell script
> docker service ls
> ```
---

> ### ▶️ Mostrar los servicios desplegados en un stack específico
> ```shell script
> docker stack ps <stack-name>
> ```
---

> ### ▶️ Detener el stack
> ```shell script
> docker stack rm <stack-name>
> ```