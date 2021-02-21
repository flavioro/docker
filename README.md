# D O C K E R - <img src="https://miro.medium.com/max/336/0*rmv6pZTW2hfP2XYd.png" alt="docker" width="150">

<!--- ![](https://miro.medium.com/max/336/0*rmv6pZTW2hfP2XYd.png) -->

* Dicionary
<p><strong>FROM</strong> - 
Inicializa o build de uma imagem a partir de uma imagem base

<p><strong>RUN</strong> - 
Executa um comando

<p><strong>LABEL</strong> - 
Adiciona metadados a imagem

<p><strong>CMD</strong> - 
Define o comando e/ou os parâmetros padrão

<p><strong>EXPOSE</strong> - 
Define que o container precisa expor a porta
em questão

<p><strong>ENV</strong> - 
Define variáveis de ambiente

<p><strong>ADD</strong> - 
Copia arquivos ou diretórios ou arquivos remotos
e adiciona ao sistema de arquivos da imagem

<p><strong>COPY</strong> - 
Copia arquivos ou diretórios e adiciona ao
sistema de arquivos da imagem

<p><strong>ENTRYPOINT</strong> - 
Ajuda você a configurar um contêiner que
pode ser executado como um executável

<p><strong>VOLUME</strong> - 
Define volumes que devem ser definidos

<p><strong>WORKDIR</strong> - 
Define o seu diretório corrente

## COMMANDS TO WORK WITH IMAGES DOCKER
* Baixa a imagem para a máquina local
```
docker pull <NOME_IMAGEM>
```

* Remove imagens não utilizadas
```
docker image prune
```

* Baixa a imagem para a máquina local
```
docker build -t <NOME_IMAGEM> -f <PATH_DO_ARQUIVO> PATH 
```

* Altera a tag de uma imagem
```
docker tag <NOME_IMAGEM> <NOVO_NOME_IMAGEM>
docker tag flavioro/temperature-conversion:v1 flavioro/temperature-conversion:lasted
```

## ADMINISTRATION CONTAINERS
```
docker container delete
docker container stop
docker container start
Docker container stats
docker run -it ubuntu /bin/bash
docker run -p 8080:80 -d nginx
```
![#f03c15](http://www.markbuckler.com/img/docker_high_level.png)

- Create container local, flavioro is name in hub.docker.com
```docker build -t flavioro/temperature-conversion:v1 . ```

- Upload container net
```
docker login  
docker push flavioro/temperature-conversion:v1
```
- Create container basead tag existent
```docker tag flavioro/temperature-conversion:v1 flavioro/temperature-conversion:latest```

- List all images
```docker image ls```

- Remove container
```docker container rm id-container```

- Remove image (different of container)
```docker rmi id-container```


- Remove container, even though it's running -f
```docker container rm -f id-container```

- Download postgres with password docker in port 5432:5432
``` docker run --name postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres```

``` docker run --name mongodb -p 27017:27017 -d -t mongo```

``` docker run --name redisdb -p 6379:6379 -d -t redis:alpine```

** Run container and release typing use -d**
``` docker container -d ngnix ```

** Access container after create, use:**
``` docker container exec -it id-Container /bin/bash```

**interface gráfica mongodb compass community**
``` login: mongodb://localhost:27017```

** Image with better security https://github.com/bitnami/bitnami-docker-postgresql
``` docker run -d --name postgres -e POSTGRESQL_USERNAME=postgres -e POSTGRESQL_PASSWORD=6153d0f22a30ad12f9963c0a081c6351 -e POSTGRESQL_DATABASE=archshop -p 5432:5432 bitnami/postgresql:latest```

Always restart container docker
```docker update --restart=unless-stopped container_id```

**L I N U X - Ubuntu**
 ``` docker container run -it ubuntu /bin/bash```

**L I N U X - Centos Update docker**
 ``` 
 yum update docker
 yum install docker-ce docker-ce-cli containerd.io
 ```
 
 **L I N U X - Version Docker**
 ``` 
systemctl status docker
 ```
 
 **L I N U X - Restart service docker**
 ``` 
 systemctl restart docker
 ``` 

* Image original postgres
``` 
docker run --name postgres -e POSTGRES_USER=postgres -e POSTGRES_DB=archshop -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres
``` 
