Return to [README](README.md) \
Return to [skill tree](skill_tree.md)

# Docker Lifecycle Exercise

Explore published docker images at https:///hub.docker.com, pull and modify upstream Dockerfiles, build, run and push local images to a private repository.

* Visit https://hub.docker.com/_/nginx in your browser for official Nginx docker images

* Select *mainline* to view latest release of Dockerfile in main branch

* Pull upstream Git repository and navigate to mainline Dockerfile
  1. `git clone https://github.com/nginxinc/docker-nginx.git`
  1. `cd cd docker-nginx/mainline/debian/`

* Open and examin Dockerfile
  1. `vim Dockerfile`
* Copy upstream docker image from Dockerfile
  1. `FROM debian:bookworm-slim`
* Familiarize yourself with Dockerfile [best practices](https://docs.docker.com/guides/workshop/09_image_best/)
* In an empty directory create a fresh Dockerfile using base image from upstream Dockerfile.
  1. `echo 'FROM debian:bookworm-slim' > Dockerfile`
* Build docker image from new Dockerfile
  1. `docker build -t debian:local .`
* Create docker container from local image and enter container.
  1. `docker run -it debian:local bash`
* Install nginx and dependencies
  1. ``
* Exit container
  1. ``
* relaunch container
  1. ``
* Run nginx
  1. ``
* Write simple command list script to re-install nginx 
  1. ``
* Update Dockerfile to include script and web content
  1. ``
* Build docker image from new Dockerfile
  1. `docker build -t nginx:local .`
* Test local container
  1. ``
* Push Dockerfile to git repository
  1. ``
* Save container to new image
  1. ` nginx:USERNAME`
* Authenticate to prvate registry
  1. ``
* Push container to private registry 
  1. ``
* Run container from image registry mounting local web content repository
  1. ``

