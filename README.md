# D O C K E R - ![](https://miro.medium.com/max/336/0*rmv6pZTW2hfP2XYd.png)

**Commands docker**

- docker run --name postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

- docker run --name mongodb -p 27017:27017 -d -t mongo

- docker run --name redisdb -p 6379:6379 -d -t redis:alpine

**interface gráfica mongodb compass community**
- login: mongodb://localhost:27017

** Image with better security https://github.com/bitnami/bitnami-docker-postgresql
- docker run -d --name postgres -e POSTGRESQL_USERNAME=postgres -e POSTGRESQL_PASSWORD=6153d0f22a30ad12f9963c0a081c6351 -e POSTGRESQL_DATABASE=archshop -p 5432:5432 bitnami/postgresql:latest

Always restart container docker
docker update --restart=unless-stopped container_id
