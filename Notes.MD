docker ps -->> running containers

dcoker images or docker image ls

docker pull nginx
docker create nginx

docker ps -a will show all the containers means running and stopped

docker start container id or image name

docker rm container id
docker rmi image name
docker rm -f container id it will forcebly delete the service

docker run nginx:tag [pull image+create container+start container]
we need to give -d detached mode then it will run in background otherwise it will run in foreground

ports : 0-65535 ports will be there

docker run -d -p 80:80 nginx
docker run -d -p 80:80 --name apple nginx

we cant run same hostport morethan one time
so host port should be always differ

docker ps -a -q [we can see all container
docker rm -f `docker ps -a -q` [it will delete all the containers]

container name also should be different

docker exec -t nginx bash [terminal] with this we can login container in docker

nginx default html path is `/usr/share/nginx/html/index.html

docker inspect container id [here we can check all the contaner details along with container ip address]

docker logs container id or container name


FROM : this is the first instruction in dockerfile for base image

docker build -t from:v1 . -->> current directory has dockerfile

