FROM maven:alpine
MAINTAINER hyness <hyness@freshlegacycode.org>

EXPOSE 8888
COPY . /opt/spring-cloud-config-server/
WORKDIR /opt/spring-cloud-config-server/
RUN mvn package
VOLUME /config
WORKDIR /
ADD target/config-0.0.1-SNAPSHOT.jar /usr/src/app.jar
ENTRYPOINT ["java", "-jar", "/usr/src/app.jar"]