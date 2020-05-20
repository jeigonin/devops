 
#TP 1 


Are you able to contact your SpringBook application through a web browser?
J'ai l'impression qu'au moment de run springboot le lancement ne se finit pas, il reste sur "Started DemoApplication in 2.436 seconds"
Did you notice that maven downloads all libraries on every image build? 
oui surtout quand on a une mauvaise connexion on s'en rend vite compte

You can contribute to saving the planet caching libraries when maven pom file has not been changed by running the goal: mvn dependency:go-offline.
Bien pensé, gain de temps en plus de ça;


    docker run --name tp1-db1 -d -e POSTGRES_PASSWORD=pwd -p 5432:5432 postgres
    url: "jdbc:postgresql://tp1-db1:5432/db"
    docker network create devops-net
    docker network connect devops-net db1-tp1
    docker run -d -p 8081:8080 --name simple-api --network=devops-net simple-app


Ask yourself: what are the useful docker-compose sub-commands?

Docker compose est utile car on peut lier facilement plusieurs images, et aussi au meme réseau par exemple, en un fichier on visualise plus facilement tout ce qui doit s'emboiter correctement


#TP2

export JAVA_HOME=$(/usr/libexec/java_home -v 1.7)

Ok, what is it supposed to do ?

Build the java project

What are Unit tests ? Integration test ?
Unit test is to verify that all functions are working each as unit
Integration test is to verify that there are not loss before updating the code version

What is a db changelog job ?

This is a report of changing structure of a database, including add table delete fields... like git changelog for important code update

What are testcontainers?

The testcontainer is the container where the project is tested while building, if it fails the build will fail and tell why and where test are not ok 


Working CI with travis file.

travis file is the entry point of travis interraction.


Why do we need this branch ?

Because before push in production branch we need to test it in development environnement and so in with dev branch

Secured variables, why ?

For allows you to authentify without any risk 

Why do we need this ?

To create at same time 

For what purpose ?

On publish the build is automticly created 

Working quality gate.

Quality is important, for maintaining and prevent breach and/or attack