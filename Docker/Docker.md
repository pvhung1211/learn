Docker is like a shipping container, but for software. Here's what it does:

### Packaging:
- It lets you package your application and everything it needs (code, libraries, dependencies) into one standardized unit called a "[[Container]]"
- Think of it like a complete box with everything your app needs to run

### Portability:
- These containers can run anywhere that has Docker installed
- Works the same way on your laptop, a server, or in the cloud
- No more "it works on my machine" problems

### Isolation:
- Each container runs separately from others
- Apps don't interfere with each other
- Makes it safer and more reliable

### Benefits:
- Easy to move applications between computers
- Quick to start and stop
- Uses less resources than traditional virtual machines
- Great for development and testing
- Perfect for microservices architecture

### Key concepts
##### [[Container]]
- Lightweight, standalone package
- Contains everything needed to run an app
- Like a mini-computer with your app inside
##### [[Image]]
- Blueprint/template for containers
- Read-only
- Used to create containers
- Can be shared/downloaded from Docker Hub

##### [[Dockerfile]]
- Text file with instructions
- Recipe to build an image
- Contains commands like FROM, COPY, RUN
- Defines how your image should be built

##### Docker Hub
- Cloud repository for Docker images
- Like GitHub but for Docker images
- Can share/download pre-made images

##### Docker Registry
- Where images are stored
- Docker Hub is the public registry
- Companies can have private registries

##### Docker Compose
- Tool to run multiple containers
- Defined in docker-compose.yml
- Makes managing multi-container apps easier

##### Volume
- Way to store persistent data
- Data survives even if container stops
- Shared storage between containers

##### [[Image vs Container]]
##### [[Docker Daemon]]
##### [[Docker Network]]

##### Layer
- Images are built in layers
- Each instruction creates a layer
- Layers can be cached and reused

