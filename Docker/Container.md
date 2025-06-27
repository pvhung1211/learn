
```bash
docker container --help

# download image `nginx` from docker hub, start the container and route comming request from host to container 
docker container run --publish 80:80 nginx

# Run in background
docker container run --publish 80:80 --detach nginx

# start: start a stopped one
# run: start a new container 
docker container start <nice_wright>

# List running containers
docker container ls

# List all containers
docker container ls -a

# logging
docker container logs <nice_wright>

# display running process of a container
docker container top <nic_wright>

# performance stats for all containers
docker container stats <nic_wright>

# display details of one container config
docker container inspect <nic_wright>

# start new container interactively
docker container run -it

# run additional command in existing/running container
docker container exec -it

# start a stopped container in detach + iteractive mode
docker container start -ai 

# Restart a container
docker container restart

# remove n container
docker container rm 46d c4 51 
docker container rm 46d -f #force

```


#### -d -it : 
- The container will be detached, we can **won't see the interactive shell immediately**, but the opened terminal process (via `-it`) keeps the container running

#### -d
- runs a container in the background (if you wish to interact with the container immediately after its creation, don't use detach)

### -it
- -i: The `-i` (interactive) flag in Docker is used to keep **STDIN** open even if not attached to the container. It's often used together with `-t` as `-it` for interactive processes like a shell.
- -t: Allocate a [[Pseudo-tty]]
### -ai
- -a: Attach **STDOUT/STDERR** and forward signals
- -i: Attach container's **STDIN**

### What happens in  "docker container run"
- Looks for that image locally in image cache, doesn't find anything
- Then looks in remote image repository (defaults Docker Hub)
- Downloads the latest version (by default)
- Create new container based on that image and prepares to start
- Give it a virtual IP on a private network inside docker engine
- Opens up port 80 on host and forwards to port 80 in container

