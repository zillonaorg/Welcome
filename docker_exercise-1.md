Return to [README](README.md) \
Return to [skill tree](skill_tree.md)

# Docker Lifecycle Exercise

Explore published docker images at https:///hub.docker.com, pull and modify upstream Dockerfiles, build, run and push local images to a private repository.

* Explore the differences between instructions, images and containers.

* Visit https://hub.docker.com/_/nginx in your browser for official Nginx docker images

* Select *mainline* to view latest release of Dockerfile in main branch

* Pull upstream Git repository and navigate to mainline Dockerfile
  1. `git clone https://github.com/nginxinc/docker-nginx.git`
  1. `cd docker-nginx/mainline/debian/`

* Open and examin Dockerfile
  1. `vim Dockerfile`

* Copy upstream docker image from Dockerfile
  1. `FROM debian:bookworm-slim`

* Familiarize yourself with Dockerfile [best practices](https://docs.docker.com/guides/workshop/09_image_best/)

* Make a new branch of this repository
  1. `git checkout -b $YOUR_NAME`

* In a new directory create a fresh Dockerfile using base image from upstream Dockerfile.
  1. `mkdir docker`
  1. `cd ./docker`
  1. `echo 'FROM debian:bookworm-slim' > Dockerfile`

* Build docker image from new Dockerfile
  1. `docker build -t debian:local .`

* Create docker container from local image and enter container.
  1. `docker run -it debian:local bash`

* Install nginx and dependencies
  1. `apt update && apt upgrade -y`
  1. `apt install -y nginx`

* Start Nginx service
  1. `nginx`

* Test Nginx from your workstation
  1. `curl localhost`

* Exit container
  1. `exit`

* relaunch container
  1. `docker run -it debian:local bash`

* Start Nginx service
  1. `nginx`

* Add commands to re-install nginx to Dockerfile
  1. `RUN apt update && apt upgrade -y`
  1. `RUN apt install -y nginx`

* Add CMD line to bottom of Dockerfile to run nginx in container
  1. `CMD ["nginx"]`

* Build docker image from your new Dockerfile
  1. `docker build -t nginx:local .`

* relaunch container
  1. `docker run -d nginx:local`

* Test local container from your workstation
  1. `curl localhost`

* Push Dockerfile to git repository
  1. `git add docker/Dockerfile`
  1. `git commit -m "Add Dockerfile"`
  1. `git push`

* Save container to new image
  1. `docker tag nginx:local registry.gitlab.com/zillona-dojo/nginx:$YOUR_NAME`

* Authenticate to prvate registry
  1. `docker login registry.gitlab.com`

* Push container to private registry 
  1. `docker push registry.gitlab.com/zillona-dojo/nginx:$YOUR_NAME`

* Clone website repository and run container from image registry mounting local web content
  1. `git clone https://gitlab.com/zillona-dojo/website.git`
  1. `docker run -dv ${PWD}:/usr/share/nginx/html registry.gitlab.com/zillona-dojo/nginx:$YOUR_NAME`

