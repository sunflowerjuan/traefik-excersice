# TAREA TRAEFIK

## Paso 1. Verificar requisitos

Ejecutamos en la terminal docker --version y docker compose version.
salida de la terminal con las versiones de Docker y Docker Compose.

![docker version](img/version.png)

## Paso 2. Levantar Traefik:

Creamos el [docker-compose.yml](docker-compose.yml) con la configuracion minima y ejecutamos docker compose up -d para iniciar Traefik.
salida de docker compose ps mostrando que Traefik está corriendo.

![docker ps](img/compose-ps.png)

## Paso 3. Acceder al dashboard de Traefik:

Abrimos en el navegador la URL http://localhost:8080/dashboard.
Dashboard de Traefik abierto en el navegador.

![docker ps](img/traefik-dashboard.png)

## Paso 4. Desplegar la aplicación de ejemplo:

Levantar el servicio de prueba (whoami) que se encuentra en el archivo [whoami.yml](whoami.yml) para que Traefik lo detecte.
terminal mostrando que el servicio de prueba se levantó correctamente.

![docker ps](img/whoami-cli.png)

## Paso 5. Probar acceso a la aplicación:

Accedemos en el navegador a http://whoami.localhost, Se muestra a continuacion la evidencia de la respuesta de la aplicación (hostname o IP del contenedor).

![docker ps](img/whoami-red.png)

## Paso 6. Revisar routers en el dashboard:

Vamos al dashboard de Traefik a la sección HTTP Routers y confirmamos que aparece whoami.localhost. a continuacon se muestra el Dashboard con el router creado para la aplicación.

![docker ps](img/whoami-traefik.png)
