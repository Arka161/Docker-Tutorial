# Docker Compose: 

Docker Compose allows us to be more efficient at what we are trying to do, and it also supports multiple containers or instances in the same application, easily bind a mount and do a lot of other things. 

Basically, we leverage a `.YAML` file, which allows us to easily write a markup for us to design our application's containerization features and their hierarchy. 

Compose is basically a three-step process: 

- We can define our app's environment using a `DockerFile`, so it can be reproduced anywhere. 
- Define the services in `docker-compose-yml`, and we can define the isolation paradigms needed as well. 
- Run the whole multi container application using `docker compose up` or `docker-compose up`. 

One sample use for Compose is connecting the front-end and back-end together, where they both run in independent containers, as highlighted [here](https://github.com/Arka161/tutorials/tree/master/docker/02-docker-compose). But some other use-cases are: 

- On one CI server, we can use Docker to containerize different builds, so that there's zero interference. 
- Creating multiple copies of the same environment, easy re-duplication. 
- Easier automated testing or unit testing.
