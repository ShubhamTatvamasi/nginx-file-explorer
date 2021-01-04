# nginx-file-explorer

[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/shubhamtatvamasi/nginx-file-explorer)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Image Version (latest semver)](https://img.shields.io/docker/v/shubhamtatvamasi/nginx-file-explorer?sort=semver)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/shubhamtatvamasi/nginx-file-explorer/latest)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Pulls](https://img.shields.io/docker/pulls/shubhamtatvamasi/nginx-file-explorer)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/shubhamtatvamasi/nginx-file-explorer/latest)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/shubhamtatvamasi/nginx-file-explorer)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)

Start the server
```bash
docker-compose up -d
```

check your local ip
```bash
ipconfig getifaddr en0
```
> this commands is for macOS
---

build docker image:
```bash
docker build -t shubhamtatvamasi/nginx-file-explorer .
```

start the container:
```bash
docker run --name nginx -d -p 80:80 -v ${PWD}:/home/:ro shubhamtatvamasi/nginx-file-explorer
```

---

start docker container in some other folder
```bash
docker run --name nginx -d -p 80:80 -v ${PWD}:/home/:ro \
-v /Users/shubhamtatvamasi/myFiles/git/nginx-file-explorer/nginx.conf:/etc/nginx/conf.d/default.conf:ro \
nginx:alpine
```

Linux process
```bash
docker run --name nginx -d -p 80:80 -v ${PWD}:/home/:ro \
  -v /home/shubham/git/nginx-file-explorer/nginx.conf:/etc/nginx/conf.d/default.conf:ro \
  nginx:alpine
```

remove the docker container
```bash
docker rm -f nginx
```
