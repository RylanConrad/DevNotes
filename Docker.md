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



- docker con