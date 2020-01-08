# nginx-file-explorer

Start the server
```bash
docker-compose up -d
```

this commands is for macOS

check your local ip
```bash
ipconfig getifaddr en0
```
---

start docker container in some other folder
```bash
docker run --name nginx -d -p 80:80 -v ${PWD}:/home/:ro \
-v /Users/shubhamtatvamasi/myFiles/git/nginx-file-explorer/nginx.conf:/etc/nginx/conf.d/default.conf:ro \
nginx:stable
```

remove the docker container
```bash
docker rm -f nginx
```
