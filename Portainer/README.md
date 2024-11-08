# Portainer

## Instalar Porteiner

```bash
docker volume create portainer_data

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

## En caso de que no olvide el pass de portainer seguir los siguientes pasos:

### detener proceso y borrar portainer:

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
