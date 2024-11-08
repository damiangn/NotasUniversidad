# VoD Server

## Descargar los el Dockerfile y la carpeta htdocs y dejarlos en el mismo directorio.

## Descargar una imagen ubuntu que tenga un apache2. Hacer esto ejecutando el Dockerfile:

```bash
docker build -t "nombre_imagen"
```

## Ejecutar un contenedor usando esa imagen:

```bash
docker run -it -v "directorio"/htdocs/:/var/www/html/ --name VoDServer --restart always "nombre_imagen"
```

**nombre_imagen** darle un nombre a la imagen
**directorio** Poner el directorio donde se encuentran el Dockerfile y la carpeta htdocs

