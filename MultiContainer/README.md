# Multi-container Application

#### Single container Deployment Issue
    - The app was simple - no outside dependencies
    - The image was build multiple times
    - How to connect a DB from a container

### Building a Fibonacci Calculator

    - Backend Architechture inclcudes
        - Nginix server is going to some routing based on user request
        - The frontend request are routed to React server
        - The backend request is routed to Express server which is connected to a Redis and Postgres server

    Architecture:
    

![Image of Architecture](https://github.com/gopswamy/DockerLearnings/blob/master/MultiContainer/image.JPG)

The images are build and passed to Travis CI for testing purposes. The images are pushed to docker hub which would be pulled by AWS to run our server.

    - Container definitions file is written for AWS to run the Docker image
