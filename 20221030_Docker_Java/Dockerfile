FROM openjdk:17
ARG JAR_FILE=spring-boot-docker/build/libs/*.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]
