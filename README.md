# nginx-file-explorer

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
