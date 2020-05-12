FROM openjdk:11
# Build Main.java
# ...

FROM openjdk:11-jre
# Copy resource from previous stage
COPY Main.class /usr/src/app
# Run java code with the JRE
CMD ["java", "Main"]