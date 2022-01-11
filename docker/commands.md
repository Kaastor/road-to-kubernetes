# Docker

* `docker run --name kubia-container -p 8080:8080 -d kubia` - run a new containter with name 'kubia-container',
  map port 8080 from local to container 8080, use 'kubia' image
* `docker inspect [container-name]` - container information
* `docker exec -it kubia-container bash` - log into the container
* `docker stop [container-name]`
* `docker em [container-name]`
* `docker build -t luksa/fortune .` - Build image with specific tag, from resources in current dir