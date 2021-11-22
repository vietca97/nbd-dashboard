FROM openjdk:8
ADD target/nbd-identity.jar nbd-identity.jar
EXPOSE 8088
ENTRYPOINT ["java","-jar","nbd-identity.jar"]