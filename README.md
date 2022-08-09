# docker_python3
Containerized Python Development


# We have now the following structure:
 ```
docker_python3/
  ├ Dockerfile
  ├ docker-compose.yml
  └ opt/
    └ sample.py
```

# Run Build Docker

```
$ cd docker-python3/
$ docker compose up -d --build
```

# Check Docker Images 
```
$ docker image ls
```

# Connect Docker Images
```
$ docker compose exec python3 bash
```

# End Docker 
```
$ exit
```

```
$ docker compose down
```

```
$ docker container ls
```

# 
$ docker compose up -d
