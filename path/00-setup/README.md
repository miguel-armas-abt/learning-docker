# CONFIGURACIÓN

[← Regresar a notas](../../README.md) <br>

----

> ### ▶️ Mostrar información de Docker
> ```shell script
> docker info
> ```

> ### ▶️ Asignar recursos a Docker Desktop
> Cree un archivo `.wslconfig` en la ruta `C:\Users\<username>\`, añada el siguiente contenido según los recursos de su computadora y reinicie Docker Desktop.
> ```javascript
> [wsl2]
> memory=3072MB
> processors=5
> ```

> ### ▶️ Eliminar todos los recursos sin utilizar (imágenes, contenedores, volúmenes y redes)
> - Utilice `--all`para especificar a todos los recursos, incluyendo los que están actualmente en uso
> ```shell script
> docker system prune --all
> ```