FROM maven:3.8.6-jdk-11

WORKDIR /workdir

COPY ./ ./

RUN mvn package && cp mall-admin/target/*.jar mall-admin/target/app.jar

EXPOSE 8080

CMD ["sh", "-c", "java -jar -Dspring.profiles.active=prod mall-admin/target/app.jar"]
