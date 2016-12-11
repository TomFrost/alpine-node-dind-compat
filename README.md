# alpine-node-dind-compat
An alpine-node docker image, including automatic compatibility with linked docker-in-docker containers.

## How to use
Start a dind container:

```
docker run --privileged --name dind-box -d docker:dind
```

Now start this container, and link dind in:

```
docker run --rm -it --link dind-box:docker tomfrost/alpine-node-dimd-compat /bin/sh
```

Now that you're inside the container, `docker ps` works and `node` is available!

## Precaution
This is not an actively maintained reposity and was created for personal use only. Feel free to fork or copy as necessary.

## Credits
The image was heavily based on https://hub.docker.com/r/mhart/alpine-node/  
alpine-node-dind-compat was created by Tom Shawver in December 2016

