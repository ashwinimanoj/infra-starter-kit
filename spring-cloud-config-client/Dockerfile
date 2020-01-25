FROM openjdk:8-jdk-alpine
ARG ARG_CONFIG_SERVER_URL
ARG JAR_FILE=target/*.jar
ENV CONFIG_SERVER_URL=$ARG_CONFIG_SERVER_URL
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java", "-jar", "/app.jar", "--spring.cloud.config.uri=${CONFIG_SERVER_URL}"]
