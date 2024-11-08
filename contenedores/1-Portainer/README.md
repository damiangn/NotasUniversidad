# Portainer

## Instalar Porteiner

```bash
docker volume create portainer_data

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

## En caso de olvidare el usuario/pass de portainer seguir los siguientes pasos:

### detener proceso y borrar portainer junto a su volumen:

```bash
docker stop portainer

docker rm portainer

docker volume rm portainer_data
```

### Reinstalar portainer:

```bash
docker run -d -p 8000:8000 -p 9443:9443 --name=portainer \
   --restart=always \
   -v /var/run/docker.sock:/var/run/docker.sock \
   -v portainer_data:/data \
   portainer/portainer-ce:latest

```

## Iniciar portainer

Dirigirse al navegador Web y escribir (https://localhost:9443)

En caso de tener otro puerto cambiar 9443 por ese puerto.
