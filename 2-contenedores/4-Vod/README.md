# VoD Server

Descargar el Dockerfile y la carpeta htdocs. Ubicarlos en el mismo directorio.

### Descargar una imagen ubuntu que tenga un apache2. Hacer esto ejecutando el Dockerfile:

```bash
docker build -t "nombre_imagen" .
```

### Ejecutar un contenedor usando esa imagen:

```bash
docker run -it -v "directorio"/htdocs/:/var/www/html/ --name VoDServer --restart always "nombre_imagen"
```

**nombre_imagen:** darle un nombre a la imagen

**directorio:** Poner el directorio donde se encuentran el Dockerfile y la carpeta htdocs

`-v "directorio"/htdocs/:/var/www/html/`: Monta un volumen. En este caso, el
directorio local `"directorio"/htdocs/` se monta en el contenedor en la ruta 
`/var/www/html/`. Esto permite compartir archivos entre tu sistema local y el contenedor. De
este modo, cualquier cambio en `"directorio"/htdocs/` se reflejará en el 
contenedor y viceversa.

Un ejemplo de directorio sería: 

```bash
docker run -it -v ~/Descargas/catv/VoDServer/htdocs/:/var/www/html/ --name VoDServer --restart always "nombre_imagen"
```
