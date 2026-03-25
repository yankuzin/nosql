 1.INTRODUCTION – PRACTICE ENVIRONMENTS FOR EPAM BIG DATA COURSE
Practice environments are based on Docker containers, which can be downloaded and invoked on the student machines.
To minimize resources, most topics will have their own dockers, running only the minimum required components
For each Docker it will be stated what is the optimal resource allocation and what is the minimum resource requirements for 
using it.

2.PREREQUISITES FOR RUNNING THE PRACTICE ENVIRONMENT
Docker
Install Docker
•Mac: https://docs.docker.com/docker -for-mac/install/
•Wind ows:  https://docs.docker.com/docker -for-windows/install/
•Linux:  https://docs.docker.com/engine/install/  (Choose your Linux distrib ution)
Configure Docker
•Open Docker settings, and configure to 8GB RAM
•For more details see here:
•Mac: https://docs.docker.com/docker -for-mac/
•Windows: https://docs.docker.com/docker -for-windows/
Install Docker Compose  (Linux only) :
•Mac & Windows: Docker compose already included along with Docker Desktop.
•Linux:  https://docs.docker.com/compose/ins tall/
Minimum system requirements
8 GB RAM
2GHz CPU
10GB free space on hard disk

3.CREATING  THE MONGODB  DOCKER CONTAINER
To install the Docker contai ner for the MongoDB  practice , run the following command  -  `
Be sure to change the IP address to the IP you previously marked
docker create --name mongo -it mongo  
This can take anywhere from 2 minutes up to an hour, depending on your internet connection.  

4.STARTING THE MONGODB  DOCKER CONTAINER
Start the Docker container using the following command:
docker start mongo
Make sure t he image is up and running:
docker ps -a

5.CONNECTING TO THE DOCKER ENVIRONMENT
Open the command prompt and issue the following  command :
docker exec -it mongo  /bin/bash

6.USEFUL DOCKER COMMANDS
VIEW DOCKER CONTAINERS AND THEIR STATUS
  docker ps -a 
STOPPING AND STARTING THE DOCKER CONTAINER  
docker st op mongo  
docker start mongo  
REMOVE A PREVIOUSLY INSTALLED DOCKER CONTAINER  
docker rm mongo  
CHECK CONTAINER RESOURCE USAGE  (RAM ETC)  
docker stats   
 
7.STOPPING  THE DOCKER ENVIRONMENT
Run command  -docker stop mongo

8.MONGODB E NVIRONMENT DETAILS
# Use root/example  as user/password  credentials  
services:  
  mongo: 
 image: mongo 
 restart:  always 
 environment:  
 MONGO_INITDB_ROOT_USERNAME:  root 
 MONGO_INITDB_ROOT_PASSWORD:  example 
  mongo-express:  
 image: mongo-express 
 restart:  always 
 ports: 
-8081:8081
 environment:  
 ME_CONFIG_MONGODB_ADMINUSERNAME:  root 
 ME_CONFIG_MONGODB_ADMINPASSWORD:  example 

9.TROUBLESHOOTI NG THE DOCKER ENVIRONMENT



