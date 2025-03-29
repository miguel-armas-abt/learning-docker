# CONTENEDORES

[← Regresar a notas](../../README.md) <br>

----

Un contenedor de Docker es la instancia en ejecución de una imagen, que aísla la aplicación y sus procesos en un entorno ligero y estandarizado. Utiliza las configuraciones y dependencias definidas en la imagen para garantizar una ejecución consistente y reproducible en cualquier entorno.

> ### ▶️ Ejecutar contenedor
> - Utilice `--rm` para eliminar el contenedor cuando se detenga
> - Utilice `-d` para ejecutar el contenedor en segundo plano
> - Utilice opcionalmente `--network <network-name>` para especificar una red personalizada
> ```shell script
> docker run --rm -p <local-port>:<internal-port> --name <container-name> <image-name:tag>
> docker run --rm -p <local-port>:<internal-port> --name <container-name> --network <network-name> <image-name:tag>
> ```
---

> ### ▶️ Mostrar los contenedores:
> ```shell script
> docker ps -a
> docker ps -a --format "table {{.ID}}\t{{.Names}}\t{{.Status}}"
> ```
---

> ### ▶️ Mostrar métricas de consumo
> ```shell script
> docker stats <container-id>
> ```
---

> ### ▶️ Mostrar logs
> - Utilice `-f` para seguir (follow) los logs en primer plano
> ```shell script
> docker logs -f <container-id>
> ```
---

> ### ▶️ Ingresar al sistema de archivos de un contenedor en ejecución
> - `it` habilita la opción de "interactivo" y asigna una terminal TTY para la sesión
> - `sh` abrir una sesión de shell
> - `bash` abrir una sesión de bash
> ```shell script
> docker exec -it <container-id> bash
> ```

> ### ▶️ Inspeccionar características del contenedor:
> ```shell script
> docker inspect <container-id>
> ```
---

> ### ▶️ Detener contenedor
> ```shell script
> docker stop <container-id>
> docker stop $(docker ps -a -q) # detener todos los contenedores
> ```
---

> ### ▶️ Iniciar un contenedor
> ```shell script
> docker start <container-id>
> ```
---

> ### ▶️ Eliminar contenedor
> Utilice `-f` (equivalente a `--force`) para forzar la eliminación
> ```shell script
> docker rm <container-id> -f
> ```
---

> ### ▶️ Eliminar los contenedores detenidos
> ```shell script
> docker container prune -f -a
> ```
---

> ### ▶️ Agregar un contenedor a la red de otro
> ```shell script
> docker network connect <container1-id> <container2-id>
> ```
---