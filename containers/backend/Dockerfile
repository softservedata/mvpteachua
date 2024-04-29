FROM alpine:latest

RUN apk update && apk add openjdk17 && apk add maven && apk add ttf-dejavu && apk add xvfb

WORKDIR /root/
COPY ./backend/ ./

RUN mvn clean package

EXPOSE 8080
ENTRYPOINT ["java","-Djava.awt.headless=true","-jar","target/dev.war"]
