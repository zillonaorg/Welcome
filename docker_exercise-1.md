Return to [README](README.md) \
Return to [skill tree](skill_tree.md)

# Docker Lifecycle Exercise

Explore published docker images at https:///hub.docker.com, pull and modify upstream Dockerfiles, build, run and push local images to a private repository.

* Visit https://hub.docker.com/_/nginx in your browser for official Nginx docker images
* Select *mainline* to view latest release of Dockerfile in main branch
* Pull upstream Git repository and navigate to mainline Dockerfile
  `git clone https://github.com/nginxinc/docker-nginx.git`
  `cd cd docker-nginx/mainline/debian/`
* Open and examin Dockerfile
  `vim Dockerfile`
* Copy upstream docker image from Dockerfile
  `FROM debian:bookworm-slim`
* Familiarize yourself with Dockerfile [best practices](https://docs.docker.com/guides/workshop/09_image_best/)
* In an empty directory create a fresh Dockerfile using base image from upstream Dockerfile.
  `echo 'FROM debian:bookworm-slim' > Dockerfile`
* Build docker image from new Dockerfile
  `docker build -t debian:local .`
* Create docker container from local image and enter container.
  `docker run -it debian:local bash`
* Install nginx and dependencies
  ``
* Exit container
  ``
* relaunch container
  ``
* Run nginx
  ``
* Write simple command list script to re-install nginx 
  ``
* Update Dockerfile to include script and web content
  ``
* Build docker image from new Dockerfile
  `docker build -t nginx:local .`
* Test local container
  ``
* Push Dockerfile to git repository
  ``
* Save container to new image
  ``
* Push container to private registry 
  ``
