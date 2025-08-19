FROM gradle:8.8-jdk17 AS build
WORKDIR /app
COPY . .
WORKDIR /app/Backend/AutoSales_Agent
RUN gradle --no-daemon clean bootJar

FROM eclipse-temurin:17-jre
WORKDIR /app
COPY --from=build /app/Backend/AutoSales_Agent/build/libs/*.jar /app/app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","/app/app.jar"]
