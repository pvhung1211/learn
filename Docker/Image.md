
```bash
	# retrieves detailed information about a Docker image in JSON format
docker image inspect nginx:latest

# listing the layers that make up the image and their metadata
docker image history nginx:latest

# creates a new repository reference (`a-tag`) for the same image
# if no tag is specified, it defaults to `latest`
docker image tag nginx a-tag

# if you want to change the tag
docker image tag nginx nginx:new-tag

# changing both repository and tag
docker image tag nginx myrepo/nginx:v1

REPOSITORY         TAG       IMAGE ID
nginx             latest    5a3221f0137b
a-tag             latest    5a3221f0137b
nginx             new-tag   5a3221f0137b
myrepo/nginx      v1       5a3221f0137b



# uploads changed layers to a image registry
docker image push <changed-image>

# auth
docker login
docker logout

```

- App binaries and dependencies
- Metadata about the image data and how to run the image
- Not a complete OS, no kernel, kernel module (e.g drivers)