Docker is a tool for packaging applications on their own, so that each app has all of the dependencies, features, and libraries necessary, and is not affected by other applications. 

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