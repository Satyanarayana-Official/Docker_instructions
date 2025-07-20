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

docker pull alpine [its very less mb ]

RUN : run instruction configure in the image like installing packages, doing some configurations, etc


`RUN executes at the time of image building`


CMD is useful to run nginx or anyother service to run background it means it should not be a exited state

EX: systemctl start nginx -->> etc/systemd/system/nginx.service

CMD ["nginx","-g","daemon off;"]

-g meaning : Set global configuration directives.

COPY : copies the code from local to container

ADD :

COPY and ADD both copies the code from local to container

`1. it can directly fetch the file from internet`
`2. it can directly untar the files into container`

Docker home directory /var/lib/docker

LABEL: 
with this we can provide labels to contaienr to understand and filter the container aslo it is useful to identify the container

docker images --filter "label=NAME=Satya"
like this we can filter images also when we require

-----
## docker login
docker login -u username
and password

EXPOSE: 
will show the ports which is opened also it is purely for documentation purpose

ENV :
its just a key value pair variables and we can access them inside the container

docker run 

ENTRYPOINT :
cmd instruction can be overriden
but entrypoint we cannot overriden
`we can use combination of CMD and ENTRYPOINT for better resutls, ENTRYPOINT will have command, default args can be supplied by CMD`
You can always override default args through command line

USER:
inside the container we can change the user id from root to normal user with mentioned specifically

```
docker build -t workdir:v1 --no-chache  --progress=plain .
```

WORKDIR :
We can setup working directory inside the container

ARG:
Arg is the variable to pass as first command before FROM
also ARG is a build time variable they can't accessed inside the container , ENV can be accessed build time and then inside the container also

docker build -t arg:v1 --progress=plan --no-cache --build-arg engineer=satya .
arg instruction variables can be overriden
