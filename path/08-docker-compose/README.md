# DOCKER COMPOSE

[← Regresar a notas](../../README.md) <br>

----

Docker Compose es una herramienta que permite definir y ejecutar aplicaciones compuestas por múltiples contenedores. Mediante un archivo YAML se especifica la configuración, redes y volúmenes, facilitando la orquestación de entornos complejos de manera sencilla y reproducible.

---

## Service
Un service representa un conjunto de configuraciones que definen cómo ejecutar uno o más contenedores de Docker.

---

📌 Utilice `-f` opcionalmente para especificar el archivo yml

> ### ▶️ Descargar las imágenes requeridas para orquestación
> ```shell script
> docker-compose pull
> ```
---

> ### ▶️ Construir las imágenes requeridas para la orquestación
> ```shell script
> docker-compose build
> ```
---

> ### ▶️ Iniciar orquestación
> - Utilice `-d` para ejecutar los contenedores en segundo plano
> - Utilice `--force-recreate` para forzar la recreación de los servicios
> - Para iniciar un servicio específico podemos agregar su nombre al final del comando
> - Utilice `--scale <service-name>=<replicas-number>` para escalar un servicio específico a una cantidad de réplicas
> ```shell script
> docker-compose up -d
> docker-compose up -d <service-name>
> docker-compose up --force-recreate -d <service-name>
> docker-compose up --scale <service-name>=<replics> -d <service-name>
> ```
---

> ### ▶️ Iniciar los servicios que aún no han iniciado
> ```shell script
> docker-compose start
> ```
---

> ### ▶️ Detener servicios de la orquestación
> ```shell script
> docker-compose stop 
> ```
---

> ### ▶️ Eliminar orquestación
> - Utilice `-v` para eliminar también los volúmenes
> ```shell script
> docker-compose down -v
> ```
---

> ### ▶️ Obtener versión
> ```shell script
> docker-compose --version
> docker compose version
> ```

