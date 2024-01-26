# Docker-examples
Practical Docker guide

## Docker CLI
### Docker file Commands

| Command        | Description           | Example  |
| -------------  |:---------------------|:---------|
| FROM           | Specifies the base image for the build| FROM ubuntu:latest |
| RUN       | Executes a command inside the container during build time | RUN apt-get update && apt-get install -y curl |
| CMD  | Specifies the default command to run when the container starts | CMD [“npm”, “start”] |
|EXPOSE|Informs Docker that the container listens on specific network ports at runtime|EXPOSE 80/tcp|
|ENV|Sets environment variables inside the container|ENV NODE_ENV=production|
|COPY|Copies files or directories from the build context into the container|COPY app.js /usr/src/app/|
|ADD|Similar to COPY but supports additional features like URL retrieval and decompression|ADD https://example.com/file.tar.gz /usr/src/|
|WORKDIR|Sets the working directory for subsequent instructions|WORKDIR /usr/src/app|
|ARG|Defines variables that users can pass at build-time to the builder with the docker build command|ARG VERSION=1.0|
|ENTRYPOINT|Configures a container to run as an executable|ENTRYPOINT [“python”, “app.py”]|
|VOLUME|Creates a mount point and assigns it to a specified volume|VOLUME /data|
|USER|Sets the user or UID to use when running the image|USER appuser|
|LABEL|Adds metadata to an image in the form of key-value pairs|LABEL version=”1.0″ maintainer=”John Doe|
|ONBUILD|Configures commands to run when the image is used as the base for another build|ONBUILD ADD . /app/src|


### Docker Volume Commands

| Command        | Description           | Example  |
| -------------  |:---------------------|:---------|
| volume create  | Creates a named volume| docker volume create mydata |
|volume ls|Lists the available volumes|docker volume ls|
|volume inspect|Displays detailed information about a volume|docker volume inspect mydata|
|volume rm|Removes one or more volumes|docker volume rm mydata|
|volume prune|Removes all unused volumes|docker volume prune|

### Container Related Commands
    docker [CMD] [OPTS] [CONTAINER]

| Command        | Description           |
| -------------  |:---------------------|
|daemon|Run the persistent process that manages containers|
|attach|Attach to a running container to view its ongoing output or to control it interactively|
|commit|Create a new image from a container’s changes|
|cp|Copy files/folders between a container and the local filesystem|
|create|Create a new container|
|diff|Inspect changes on a container’s filesystem|
|exec|Run a command in a running container|
|export|Export the contents of a container’s filesystem as a tar archive|
|kill|Kill a running container using SIGKILL or a specified si|
|logs|Fetch the logs of a container|
|pause|Pause all processes within a container|
|port|List port mappings, or look up the public-facing port that is NATed to the PRIVATE_PORT|
|ps|List containers|
|rename|Rename a container|
|restart|Restart a container|
|rm|Remove one or more containers|
|run|Run a command in a new container|
|start|Start one or more containers|
|stats|Display one or more containers’ resource usage statistics|
|stop|Stop a container by sending SIGTERM then SIGKILL after a grace period|
|top|Display the running processes of a container|
|unpause|Unpause all processes within a container|
|update|Update configuration of one or more containers|
|wait|Block until a container stops, then print its exit code|

### Image Related Commands
    docker [CMD] [OPTS] [IMAGE]
| Command        | Description           |
| -------------  |:---------------------|
|build|Build images from a Dockerfile|
|history|Show the history of an image|
|images|List images|
|import|Create an empty filesystem image and import the contents of the tarball into it|
|info|Display system-wide information|
|inspect|Return low-level information on a container or image|
|load|Load an image from a tar archive or STDIN|
|pull|Pull an image or a repository from the registry|
|push|Push an image or a repository to the registry|
|rmi|Remove one or more images|
|save|Save one or more images to a tar archive|
|search|Search one or more configured container registries for images|
|tag|Tag an image into a repository|
