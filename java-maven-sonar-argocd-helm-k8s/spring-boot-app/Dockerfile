# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM maven:3.9.11-eclipse-temurin-21

RUN apt-get update && \
    apt-get install -y git docker.io

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]

CMD ["cat"]
