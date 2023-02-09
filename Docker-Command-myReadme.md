# Docker command
1. docker run hello-world // to test the docker

    1.1 docker start <container_name> // docker ps -a // display docker list

        1.1.1 docker start grafana/grafana // port already define during run/download

        1.1.2 if want to edit port then need to edit "/var/lib/docker/containers/[hash_of_the_container]/hostconfig.json"

    1.2 docker run <container_name> // docker will initial new container , which will sit under docker ps -a . create + start

        1.2.1 docker run -d -p 3000:3000 grafana/grafana 

2. docker stack deploy -c launch-mongo.yml mongo // launch yml file for mongo and mongo express (in swarm)
3. service docker status // check docker status
4. service docker start // start docker
5. service docker stop // stop docker service
6. docker image ls  // download image comamnd => docker pull grafana/grafana
7. docker run image_name // docker run mongo example: docker run -d -p 3000:3000 --name grafana grafana/grafana
8. docker compose -f docker-compose.yml up -d       // -f = file, up = start service , -d = start service in background
9. docker exec -it kafka /bin/sh                    // -it <name_of_container>  it = interactive mode , enter inside kafka
  
    9.1 kafka binary = /opt/kafka/bin
    
    9.2 create kafka topic = ./bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic testing123
    
    9.3 list kafka topic = ./bin/kafka-topics.sh --list --zookeeper zookeeper:2181

10. docker commit <container_name>
    >> It can be useful to commit a container's file changes or settings into a new image


10. swarm
    
    10.1 docker system info // check for swarm status , swarm: active
    
    10.2 docker swarm init // setup swarm
    
    10.3 docker stack deploy -c abc.yml demo // install yml into swarm
    
    10.4 docker service ls // list all the service
    
    10.5 docker stack rm mongo // tear down appplication
 
    10.6 docker stack *
 
    12.7 docker service *
   
# Docker compose
    1. docker compose up -d  // default is docker-compose.yml
    
    2. docker compose -f docker-99.yml up -d // -f = file, up = start service , -d = start service in background

# Docker inspect
    1. docker inspect <containerID>
    
    2. docker update --restart=no <containerID> // try to disable auto start after docker restart