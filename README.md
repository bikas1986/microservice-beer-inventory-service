# microservice-beer-inventory-service
Microservices Beer Inventory Service


We will use docker to run mysql:

docker container run --name beer-inventory-service-mysql -p 3308:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_USER=beer-inventory-service-user -e MYSQL_PASSWORD=password -e MYSQL_DATABASE=beerinventoryservice -d mysql:latest

To enter the running instance of mysql using bash mode:

docker container exec -it beer-inventory-service-mysql bash

Now we are in bash mode of the container. To login to mysql server instance:

mysql -u beer-inventory-service-user -p

Now enter the password as 'password'

show databases;


-----------------------------------------------------------------
We are also using docker to run ActiveMQ Artemis

Artemis activemq Docker: 
https://github.com/vromero/activemq-artemis-docker

docker run -it --rm \
  -p 8161:8161 \
  -p 61616:61616 \
  vromero/activemq-artemis
  
  
  
To view in the console:
http://127.0.0.1:8161/  

Username = artemis

Password = simetraehcapa
