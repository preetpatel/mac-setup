# Tips and Tricks

A collection of useful tips and tricks for Docker.

## Delete all containers

**NOTE:** This will remove ALL your containers.

```bash
docker container prune
```

OR, if you're using an older docker client:

```bash
docker rm $(docker ps -a -q)
```

## Delete all untagged containers

```bash
docker image prune
```

OR, if you're using an older docker client:

```bash
docker rmi $(docker images | grep '^<none>' | awk '{print $3}')
```

## See all space Docker take up

```bash
docker system df
```

## Get IP address of running container

```bash
docker inspect [CONTAINER ID] | grep -wm1 IPAddress | cut -d '"' -f 4
```

## Kill all running containers

```bash
docker kill $(docker ps -q)
```

