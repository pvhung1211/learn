
#### Prerequisite [[Networking Fundamentals]]

#### Default port **80 (HTTP)** or **443 (HTTPS)** (if the port not be specified, it will reach these port when making HTTP requests)

#### [[Network interface]]

##### [[DNS]]

##### [[Docker DNS]]

##### [[TCP,UDP]]

#### Commands
```bash
# Show networks
docker network ls

# Inspect a network
docker network inspect

# Create a new network (with opt network driver)
docker network create --driver <my_app_net>

# Attach a network to container
docker network connect <my_app_net> <my_container>

# Detach a network from container
docker network disconnect

# Run a container on the specified network
docker run --network my_network nginx

# Give the container an alias so that others in the same network can connect to it via this alias
docker run -d --name my_container --network my_network --network-alias my_alias nginx

```

#### Defaults
- Each container connected to a private virtual network "[[Bridge]]"
- Each virtual network routes through [[NAT]] [[Firewall]] on host IP
- All containers on a virtual network can talk to each other without -p
- Best practice is to create a new virtual network for each app
	- network "my_web_app" for mysql and php/apache containers
	- network "my_api" for mongo and nodejs containers

#### Batteries included
- Make a new virtual network
- Attach containers to more than one virtual network (or none) 
- Skip virtual networks and use host IP (--net=host)
- Use different Docker network drivers to gain new abilities

#### Default Security
- Create ur apps so FE/BE sit on same Docker network
- Their inter-communication never leaves host
- All externally exposed ports closed by default
- You must manually expose via -p, which is better default securiry
- This gets even better later with Swarm and Overlay networks