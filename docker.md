# Docker

```
docker run -it --name=<name> --volume ~/volumes/<name>:/data ubuntu:jammy

docker run -it --name=<name> --volume ~/volumes/<name>:/data --expose 8080:8080 ubuntu:jammy

docker exec -it <name> bash
```

```
curl http://host.docker.internal:8080

```


```
docker run -it --name=keymaker --volume ~/volumes/keymaker:/data ubuntu:jammy

docker run -it --name=aptrepo --volume ~/volumes/aptrepo:/data --expose 8080:8080 ubuntu:jammy

docker run -it --name=target --volume ~/volumes/target:/data ubuntu:jammy
```

```
apt-key add /data/sgre-public.asc

apt update


```
