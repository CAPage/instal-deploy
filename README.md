# InstAL-Deploy
For deploying InstAL-REST easily. This is the recommended way to deploy an instance of InstAL-REST on a server. This requires Docker.

# Containers
* InstAL-DB - A postgres database container.
* InstAL-Rabbit - A RabbitMQ container.
* InstAL-REST - The container running the HTTP server that serves the API, using gunicorn.
* InstAL-Celery - The container running the celery workers that actually run InstAL.

# Instructions
* Clone this repository using the command 'git clone --recursive <repoAddress>'
* cd into the project's root directory
* Run the shell script ./fullbuild.sh
* Run one of the "up" shell scripts, either dev or production.

# More advanced setup
* You can change the production and development configuration options using docker-compose.{dev, prod}.yml. 
* You can use docker-compose scale to increase the number of each type of docker container. For instance: "docker-compose scale instal-rest=2 instal-celery=3" will run two HTTP server containers and 3 celery containers.
