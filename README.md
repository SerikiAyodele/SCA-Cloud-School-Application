# SCA-Cloud-School-Application
Technical Assessment for She Code Africa Cloud School.

## Test this project

#### 1. Build Docker image

`docker build -f docker/Dockerfile -t seriki/sca-cloud .`

#### 2. Run Docker container (on local port 8080)

`docker run -p 8080:80/tcp --name sca-cloud seriki/sca-cloud`

#### 3. Visit localhost:8080 on your browser

You should see a boilerplate React page with some text.

## DockerHub repository

https://hub.docker.com/repository/docker/seriki/sca-cloud
