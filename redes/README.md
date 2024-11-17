# Creacion de redes para los contenedores

Se deben crear las redes correspondientes a cada contenedor y desde portainer (ó puede ser desde nuestra terminal de Linux) asignarselas al que le corresponda.

Para esto escribir en una Terminal de nuestro Linux:

```bash
docker network create -d macvlan --subnet=10.0.20.0/24 --gateway=10.0.20.1 --ip-range=10.0.20.128/25 -o parent=enp3s0.20 tv
```
```bash
docker network create -d macvlan --subnet=10.0.30.0/24 --gateway=10.0.30.1 --ip-range=10.0.30.128/25 -o parent=enp3s0.30 VoIP
```

<h3>Nota:<h3> *Estos son dos ejemplos. Borrar --ip-range si no se quiere reservar un rango. En caso de no borrarlo el rango reservado corresponde, por ej:*
*--ip-range=10.0.30.128/25 el rango va desde 10.0.30.128 hasta 10.0.30.255*
