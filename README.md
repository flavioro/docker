# D O C K E R - ![](https://miro.medium.com/max/336/0*rmv6pZTW2hfP2XYd.png)

**Commands docker**

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
