# docker-debian-cockpit
Debian Linux (v11 - bullseye) running systemd and cockpit


## How to use this image:

### Run the image using docker:
- docker run -d --privileged --name debian-cockpit hurenkam/debian-cockpit:latest

And set the root password:

- docker exec -ti debian-cockpit passwd 

### Run the image using podman:
- podman run -d --privileged --name debian-cockpit docker.io/hurenkam/debian-cockpit:latest

And set the root password:

- podman exec -ti debian-cockpit passwd 

### Access cockpit or ssh
Point your browser to https://<< hostname >>:9090 where you find a running cockpit instance
or use ssh <hostname> to log into a console.

## Source:
- https://github.com/hurenkam/docker-debian-cockpit/
 
## Credits:
To get debian working with systemd, i based it on these Dockerfiles:
- https://github.com/j8r/dockerfiles/blob/master/systemd/debian/11.Dockerfile
- https://github.com/alehaa/docker-debian-systemd/blob/master/Dockerfile
