# PPS Equivalencias 2023c2

Dockerización de pps-equiv.

## Descripción

Se crean 3 contenedores. Uno con la base de datos postgresql; uno con node, este ejecuta la api del backend y otro con nginx, este funciona también como proxy para la api y así exponer toda la aplicación en un puerto.

El último contenedor se construye en dos etapas: la primera con node, corre el build y la segunda etapa copia la salida del build react a un contenedor nginx.

## Cambios

Hubo que hacer cambios menores en la configuración de la app y el config de apiURL.

## Instrucciones

Instalar docker para nuestro sistema operativo.

```
git clone --recurse-submodules ESTE_REPO
cd ESTE_REPO
git submodule update --init --recursive --remote
docker-compose build
docker-compose up -d
```

## Ver los logs

```
docker-compose logs
```

## Detener los contenedores

```
docker-compose down
```

