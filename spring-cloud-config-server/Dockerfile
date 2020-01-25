FROM openjdk:8-jdk-alpine
ARG URL
ARG JAR_FILE=target/*.jar
ENV CLOUD_CONFIG_REPO_URL=$URL
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java", "-jar", "/app.jar", "--spring.cloud.config.server.git.uri=${CLOUD_CONFIG_REPO_URL}"]
