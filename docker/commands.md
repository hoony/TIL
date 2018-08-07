## stop
: to stop the container running
: ex) `docker stop {ID}`

## rm
: to remove the container
: ex) `docker rm {ID}`

## rmi
: to remove the image
: ex) `docker rmi {ID}`

### *Tips*
: to stop, rm, rmi all containers or images, type this.
: stop, rm: `docker stop(rm) $(docker ps -aq)`
: rmi: `docker rmi $(docker images -aq)`

## `exec`
: to access the container running
: ex) `docker exec -it {ID} /bin/bash`