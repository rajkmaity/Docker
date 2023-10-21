How to use docker :

Create the network
docker network create mongo-network 


 docker run 
 -d  ## It is to run in detached mode
 -p 27017:27017  ## It is to show the host port: container port
 -e MONGO_INITDB_ROOT_USERNAME=admin   ### e : signifies the environment 
 -e MONGO_INITDB_ROOT_PASSWORD=password 
 --name mongodb   ### this what the name of the container
 --net mongo-network ## name of the network that will be connected to the container
 mongo ## name of the image from the docker hub