# kafka-conduktor.io
Connect Kafka (KRaft mode) and Conduktor.io running on Docker Desktop
I'm using the docker setup from https://docs.conduktor.io/platform/get-started/installation/get-started/docker/#simple-setup and
https://hub.docker.com/r/apache/kafka as provided on the lecture and by Stephane's TA Ivan T.

Here are the steps that I took:
Create the network first: 
```dockerfile 
docker network create kafka-net
```
Then create and start the containers inside kafka directory
```dockerfile
docker compose -f .\kafka\docker-compose.yml up -d
```
Then create and start the containers inside conduktor directory
```dockerfile
docker compose -f .\conduktor\docker-compose.yml up -d
```
Check the kafka-net network to check which containers are linked to it.
```dockerfile
docker inspect kafka-net
```
