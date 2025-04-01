# IMÁGENES

[← Regresar a notas](../../README.md) <br>

----

> ### ▶️ Construir imagen
> - Utilice `-t` para especificar el nombre de la imagen y su correspondiente tag
> - Utilice `-f` opcionalmente para especificar una ruta personalizada del Dockerfile
> - Al final del comando indique la ruta donde se encuentra la aplicación (`.` representa el directorio actual)
> ```shell script
> docker build -t <image-name:tag> .
> docker build -f ./docker/Dockerfile -t <image-name:tag> .
> docker build -f ./docker/Dockerfile -t <image-name:tag> ./../app
> ```
---

> ### ▶️ Mostrar imágenes
> - Utilice `-a` (equivalente a `--all`) para mostrar todas las imágenes del sistema
> - Utilice `-q` para mostrar solamente los IDs
> ```shell script
> docker images
> ```
---

> ### ▶️ Eliminar imagen
> - Utilice `-f` (equivalente a `--force`) para forzar la eliminación de la imagen
> ```shell script
> docker rmi <image-id> -f
> ```
---

> ### ▶️ Eliminar las dangling images `<none>`
> ```shell script
> docker images --filter "dangling=true" -q | xargs docker rmi -f
> ```
---

> ### ▶️ Eliminar todas las imágenes
> ```shell script
> docker rmi $(docker images -a -q)
> ```