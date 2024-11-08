# mumudvb

### Descargar la imagen mumudvb:

```bash
docker build -t mumudvb .
```

### Crear y ejecutar el contenedor:

```bash
docker run -t -i --device=/dev/dvb/ --name mumudvb_contenedor mumudvb
```

<h3>Nota:<h3> Abrir portainer, conectar SDR a la PC y recién ahí poner Start para iniciar el contenedor.