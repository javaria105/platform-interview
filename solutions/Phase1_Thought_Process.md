In order to complete phase 1, I first ran the code to run the application locally to see what error the 
developer could be getting. The error I complained that I did not have the correct permissions configured 
for docker to run. I assume this is why the developer could not get the application to run, but 
would probably want to talk to them to see if they received any other errors.
To help with codebase management to run this app consistently, I utilized **docker-compose**. I have a `Dockerfile`
and a `docker-compose.yml` file that I have uploaded along with this thought process. The `Dockerfile` builds
a container that copies all the files in the respoitory to a container, runs the `./gradlew bootJar`
command, and executes the newly created jar file. The `docker-compose.yml` file configures the services I need 
for my application. I then ran `docker-compose up --build` to build my configuration. Below, please find a 
screenshot of what this looked like for me and links to the resources I used to build my docker files.

Screenshot: <img width="1390" alt="Screen Shot 2022-04-27 at 10 29 27 AM" src="https://user-images.githubusercontent.com/55933082/165560787-9fdf3f5e-737b-456c-940d-5bda2457c940.png">


Resources:

https://www.baeldung.com/dockerizing-spring-boot-application

https://ashoksubburaj.medium.com/build-docker-image-using-spring-boot-buildimage-gradle-ac5bc1f71303

https://docs.docker.com/engine/reference/builder/#copy

https://docs.docker.com/language/java/build-images/
