Docker is a tool for packaging applications on their own, so that each app has all of the dependencies, features, and libraries necessary, and is not affected by other applications. 

**Refer to DockerHub for Images**

**Images**
- You boot up a container from an image
- A container is a running instance of an image
- Definitions of the App and everything that it needs to run

example - 
```bash
docker run -d -p hostport:containerport namespace/name:tag
```

- -d runs in detached mode
- -p specifies the port
- namespace/name ---- username/repo(docker/getting-started)
- tag ----- version of the image
- -e says we want to set an environment variable

**Volumes**
- Saved memory
- Lives outside of the container *but* can be accessed by the container

```shell 
docker run -d -e NODE_ENV=development -e url=http://localhost:3001 -p 3001:2368 -v ghost-vol:/var/lib/ghost ghost
```

- -p port forwarding between container and our computer.
- in this case its hosted at localhost:3001, and the container port is 2368
- Containers are typically thought of as temporary, so creating a volume makes them persistent.
- volume mounted at ghost-vol:/var/lib/ghost/content

**Live Shell**
```shell
docker exec CONTAINER_ID /bin/sh
```
puts you in a live shell on the already running container

-u 0 lets you run stuff as root 
- --network none separates the container from the network.


**Dockerfile**
- Used for building a docker Image.
- Automates the entire image creation process
- FROM: - specifies the base image to start from
- WORKDIR - sets the working directory
- COPY: copies files from local machine into the image
- RUN: Executes commands during image build
- EXPOSE: Informs docker that the container listens on the specified network ports at runtime.
- CMD: Default commands for a container("echo")