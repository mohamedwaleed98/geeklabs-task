## INTRODUCTION
   This is a very basic application that uses "react" as frontend and "nodejs" as backend and stores data in "mysql" database. The application is dockerized using "docker-compose", each service and by service I mean (frontend, backend, db, monitoring and logging tools) has its own container.


## DOCKERIZING
   Every service has its own docker file in its own directory. To run the application run: 'docker-compose --build -d'.
   All the services can communicate with each other using the same network that is configured in the same YAML file. 

## ACCESSING THE APP
   Each service works on a different port, check below the provided localhost ports to access each service:
   
      frontend:  localhost:3001
      backend:   localhost:3000
  
      prometheus: localhost:9090
      grafana:    localhost:3002

## CHALLENGES ENCOUNTERED
   -- The backend's container could not reach the mysql datbase container due to some misconfigurations in the nodejs.
   -- Couldn't fully implement grafana and prometheus into the app, deployment only.
