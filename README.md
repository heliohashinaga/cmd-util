# Util
Lista de comandos úteis.

## WCF Service Reference
Criação de Service Reference de WCF com SvcUtil
1. Abrir Developer Command Prompt for VS 20xx (versão do visual studio)
2. Executar o comando
```
svcutil http://locahost/service.svc /Language=c# /t:Code /ct:System.Collections.Generic.List`1 /out:ServiceName.cs /config:ServiceName.config 
```
## Docker

### Build

Criar uma imagem no diretório atual e tag a imagem
```
docker build -t <image name>:<tag> .
docker build -t myimage:1.0 .
```

Listar todas as imagens de docker
```
docker image ls
```

Deletar uma imagem
```
docker image rm <image name>
```
### Run

Criar um container de uma imagem
```
docker container run --name <container name> -p <external port>:<internal port> <image name>
docker container run --name web -p 5000:80 alpine:3.9
```

Listar os containers em execução
```
docker container ls
```
Listar os containers em execução e os containers parados
```
docker container ls --all
```

Executar comando dentro do container
```
docker exec -it <container name> /bin/bash
docker exec -it <container name> influx
```
