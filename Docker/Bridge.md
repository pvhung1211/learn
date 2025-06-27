
#### (In the context of Docker, it just refers to a type of virtual network)

A "bridge network" in Docker is ==a virtual network created by a software bridge that allows containers running on the same Docker host to communicate with each other while remaining isolated from other networks==, essentially acting as a dedicated network segment for containers within a single Docker instance; it's the default network mode for Docker containers, meaning when you start a container without specifying a network, it automatically joins the default bridge network.

- **Isolation:**
    Containers on different bridge networks cannot directly communicate with each other. 
- **Single host limitation:**
    Bridge networks are only suitable for containers running on the same [[Docker Host]]. 
- **Default network:**
    When you start a Docker container without specifying a network, it automatically joins the default "bridge" network. 
- **User-defined bridges:**
    You can create custom bridge networks with specific names to organize your containers.