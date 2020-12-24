# config-server

Steps to first deploy

* 01 - sudo apt-get install default-jdk
* 02 - sudo apt install maven
* 03 - sudo apt install git
* 04 - install docker -> https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository
* 05 - sudo mkdir /opt/services



Steps to build and run
* - cd /opt/services
* - sudo git clone https://github.com/eumagnun/config-server.git
* - cd config-server/config-server
* - sudo mvn install
* - sudo java -jar target/config-server-0.0.1-SNAPSHOT.jar
* - sudo docker build -t springio/gs-spring-boot-docker .
* - sudo docker run -d -p 8080:8888 springio/gs-spring-boot-docker
