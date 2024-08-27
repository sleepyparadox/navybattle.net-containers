# NavyBattle.Net Containers

These are the containers for a Kubernetes and ASP.Net tech demo

Full project at [github.com/sleepyparadox/navybattle.net](https://github.com/sleepyparadox/navybattle.net)

## Create Container images

### Build and push navybattle-api image

Build and push the navybattle-api container to your container repository

I've pushed to [sleepyparadox/navybattle-api:latest](https://hub.docker.com/repository/docker/sleepyparadox/navybattle-api) on Docker Hub

```bash
docker build -t sleepyparadox/navybattle-api:latest containers/navybattle-api
docker login
docker push sleepyparadox/navybattle-api:latest
```

### Build and push navybattle-client image

Build and push the navybattle-client container to your container repository

I've pushed to [sleepyparadox/navybattle-client:latest](https://hub.docker.com/repository/docker/sleepyparadox/navybattle-client) on Docker Hub

```bash
docker build -t sleepyparadox/navybattle-client:latest containers/navybattle-client
docker login
docker push sleepyparadox/navybattle-client:latest
```
