# Examen práctico 2

## Objetivo del proyecto

Desplegar una aplicación web en tres servicios independientes,
administrarlos con Docker Compose, controlar los cambios con Git
y GitHub y crear una visualización de datos comerciales.

## Datos del alumno

- Nombre: Aldo Dominguez Contrera
- Matrícula: 237O02069
- Grupo: A

## Imagen utilizada

La imagen propia del proyecto se llama `examen:237O02069`.

Se construye a partir del Dockerfile y utiliza Nginx Alpine
para publicar el archivo `web/index.html`.

## Puertos

| Servicio | Puerto del equipo | Puerto del contenedor |
|---|---:|---:|
| web1 | 8081 | 80 |
| web2 | 8082 | 80 |
| web3 | 8083 | 80 |

## Cómo levantar los servicios

Construir y levantar los tres servicios:

```bash
docker compose up -d --build
```

Comprobar su estado:

```bash
docker compose ps
```

Abrir la aplicación:

- http://localhost:8081
- http://localhost:8082
- http://localhost:8083

Para recuperar el segundo servicio:

```bash
docker compose up -d web2
```

Para detener los servicios al terminar las pruebas:

```bash
docker compose down
```

## Visualización

Herramienta: Microsoft Excel.

Proveedor y ecosistema: Microsoft.

El dashboard presenta las ventas por mes, los clientes por mes,
las ventas totales, el promedio de pedidos y el mes con mayores ventas.

Los datos y el archivo fuente del dashboard se encuentran
en la carpeta `visualizacion/`.
