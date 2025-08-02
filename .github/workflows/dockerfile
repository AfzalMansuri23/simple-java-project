#-------------------Stage1: Build the java app -------------------
FROM openjdk:17 AS build

WORKDIR /app

COPY Main.java .

RUN javac Main.java

#----------------SATGE2: Run the Java app -----------------------
FROM openjdk:17-slim

WORKDIR /app

COPY --from=build /app/Main.class .

CMD ["java", "Main"]