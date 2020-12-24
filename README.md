# config-server

Steps to first deploy

* 01 - sudo apt-get install default-jdk
* 02 - sudo apt install maven
* 03 - sudo apt install git
* 04 - install docker -> https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository
* 05 - sudo mkdir /opt/services
* 06 - cd /opt/services
* 07 - sudo git clone https://github.com/eumagnun/config-server.git
* 08 - cd config-server/config-server
* 09 - sudo mvn install
* 10 - sudo java -jar target/config-server-0.0.1-SNAPSHOT.jar
* 11 - sudo docker build -t springio/gs-spring-boot-docker .
* 12 - 
