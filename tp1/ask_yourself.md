 
 TP 1 

 Backend (springboot):

Are you able to contact your SpringBook application through a web browser?
J'ai l'impression qu'au moment de run springboot le lancement ne se finit pas, il reste sur "Started DemoApplication in 2.436 seconds"
Did you notice that maven downloads all libraries on every image build? 
oui surtout quand on a une mauvaise connexion on s'en rend vite compte

You can contribute to saving the planet caching libraries when maven pom file has not been changed by running the goal: mvn dependency:go-offline.
Ahh bien ca;


docker run --name tp1-db1 -d -e POSTGRES_PASSWORD=pwd -p 5432:5432 postgres
url: "jdbc:postgresql://tp1-db1:5432/db"
docker network create devops-net
docker network connect devops-net db1-tp1
docker run -d -p 8081:8080 --name simple-api --network=devops-net simple-app

