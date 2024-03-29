# nginx-file-explorer

[![docker build](https://github.com/ShubhamTatvamasi/nginx-file-explorer/actions/workflows/docker-build.yml/badge.svg)](https://github.com/ShubhamTatvamasi/nginx-file-explorer/actions/workflows/docker-build.yml)
[![Docker Image Version (latest semver)](https://img.shields.io/docker/v/shubhamtatvamasi/nginx-file-explorer?sort=semver)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/shubhamtatvamasi/nginx-file-explorer/latest)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)
[![Docker Pulls](https://img.shields.io/docker/pulls/shubhamtatvamasi/nginx-file-explorer)](https://hub.docker.com/r/shubhamtatvamasi/nginx-file-explorer)

Start the server
```bash
docker-compose up -d
```

check your local ip
```bash
# for linux
ip a

# for macOS
ipconfig getifaddr en0
```
---

build docker image:
```bash
docker build -t shubhamtatvamasi/nginx-file-explorer .
```

start the container:
```bash
docker run --name nginx -d -p 80:80 --restart unless-stopped -v ${PWD}:/home/:ro shubhamtatvamasi/nginx-file-explorer
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
