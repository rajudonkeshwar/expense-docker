docker command:
docker login -u rajudonkeshwar
docker build -t rajudonkeshwar/mysql:1.0.0
docker run -d --name mysql rajudonkeshwar/mysql:1.0.0
docker exec -it rajudonkeshwar/mysql:1.0.0 bash

mysql commands
mysql -u root -pExpenseApp@1
show databases;
use transactions;


creation of docker network:
( In docker if we use default network( bridge network ) docker containers can not communicate with each other to make communication we should create our own network )

docker network create expense
docker network ls
docker network disconnect bridge mysql
docker network disconnect bridge mysql ( here we are disconnecting mysql container from bridge network)
docker network connect expense mysql ( here we are connecting mysql container to the expense network )
