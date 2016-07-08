
## Docker Repo for my Images

### Demo Description Steps


#### Run command Docker Compose

docker-compose -f /vagrant/docker-compose.yaml up -d

#### Run command Docker PS
docker ps

#### Run command Docker Exec
docker exec -ti nginx bash
Inside container do ps aux

#### Change step
Change from image to build of nginx container

#### Run command Docker tag

docker tag vagrant_nginx carloscarvalho/nginx:latest

docker tag vagrant_nginx carloscarvalho/nginx:v2

docker tag nginx:1.9.7 carloscarvalho/nginx:v1

docker tag vagrant_node1 carloscarvalho/node:latest

docker tag vagrant_node1 carloscarvalho/node:v1

docker tag vagrant_redis carloscarvalho/redis:latest

docker tag vagrant_redis carloscarvalho/redis:v1

#### Run command Docker compose with file compose.yaml
docker-compose -f /vagrant/compose.yaml up -d

#### Change step
Change versions on compose.yaml to see differencess between images (Nginx default page and Nginx upstreaming to choose nodejs node)

#### Run command Docker Login to auth in docker registry
docker login -u "carloscarvalho"

#### Run command Docker Push to send artifacts to docker registry

docker push carloscarvalho/nginx:v1

docker push carloscarvalho/nginx:v2

docker push carloscarvalho/nginx:latest

docker push carloscarvalho/node:v1

docker push carloscarvalho/node:latest

docker push carloscarvalho/redis:v1

docker push carloscarvalho/redis:latest

#### Run command Docker compose to stop and remove containers
Do docker-compose -f /vagrant/compose.yaml stop & docker-compose -f /vagrant/compose.yaml rm

#### Run command Docker compose to remove images to give example of pulling from registry
Do docker rmi carloscarvalho/node:v1 & docker rmi carloscarvalho/node




