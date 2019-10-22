FROM maven:alpine
MAINTAINER hyness <hyness@freshlegacycode.org>

EXPOSE 8761
COPY . /opt/spring-cloud-config-server/
WORKDIR /opt/spring-cloud-config-server/
RUN mvn package
VOLUME /config
WORKDIR /
ADD eureka-0.0.1-SNAPSHOT.jar /usr/src/app.jar
ENTRYPOINT ["java", "-jar", "/usr/src/app.jar"]
