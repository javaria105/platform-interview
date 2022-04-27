FROM openjdk:11.0.14.1-jdk
COPY . /
RUN ./gradlew bootJar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/build/libs/platform-interview-0.0.1-SNAPSHOT.jar"]
