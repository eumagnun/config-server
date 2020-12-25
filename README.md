# config-server

Steps to first deploy

* 01 - install jdk 15
* -- apt get update
* -- wget https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz
* -- sudo mkdir -p /usr/java/openjdk
* -- cd /usr/java/openjdk
* -- mv /home/eumagnun/openjdk-15.0.1_linux-x64_bin.tar.gz .
* -- tar -xzvf openjdk-15.0.1_linux-x64_bin.tar.gz 
* -- sudo nano /etc/profile

* ---
* //put it at the end of file:
*
* #OpenJDK 15
* JAVA_HOME=/usr/java/openjdk/jdk-15.0.1
* PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
* export JAVA_HOME
* export PATH
* 

* -- reboot
* -- java -version
* 02 - sudo apt install maven
* 03 - sudo apt install git
* 04 - install docker -> https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository
* 05 - sudo mkdir /opt/services



Steps to build and run
* - cd /opt/services
* - sudo git clone https://github.com/eumagnun/config-server.git
* - cd config-server/config-server
* - sudo mvn install
* - sudo docker build -t eumagnun/config-server .
* - sudo docker run -d -p 8080:8888 eumagnun/config-server
