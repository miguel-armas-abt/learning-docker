# DOCKER HUB

[← Regresar a notas](../../README.md) <br>

----

[Docker Hub](https://hub.docker.com/) es una plataforma que sirve como repositorio de imágenes (registry) de Docker, la cual permite acceder y compartir imágenes.

> ### ▶️ Autenticarse con Docker Hub
> ```shell script
> docker login
> ```
---

> ### ▶️ Asignar nueva etiqueta a una imagen
> Renombra y prepara la imagen local para ser subida a DockerHub
> ```shell script
> docker tag <local-image:tag> <username/remote-image:tag>
> ```
---

> ### ▶️ Subir imagen a DockerHub:
> ```shell script
> docker push <username/remote-image:tag>
> ```
---

> ### ▶️ Descargar imagen desde DockerHub
> ```shell script
> docker pull <username/remote-image:tag>
> ```
---

> ### ▶️ Construir un contenedor a partir de una imagen descargada
> La única diferencia es que se antepone el `username/` antes de la imagen
> ```shell script
> docker run -p <local-port>:<internal-port> <username/image-name:tag>
> ```


