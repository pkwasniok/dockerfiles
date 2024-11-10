FROM ubuntu:24.10

WORKDIR /minecraft/server

RUN apt-get update && apt-get upgrade

RUN apt-get install -y wget default-jre

ARG minecraft_server_exec_url=https://piston-data.mojang.com/v1/objects/45810d238246d90e811d896f87b14695b7fb6839/server.jar

RUN wget $minecraft_server_exec_url -O server.jar

WORKDIR /minecraft/world

CMD ["java", "-jar", "-Xms512M", "-Xmx1024M", "/minecraft/server/server.jar"]

EXPOSE 25565

