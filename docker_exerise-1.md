Return to [README](README.md)
Return to [skill tree](skill_tree.md)

# Docker:

* https://hub.docker.com/_/nginx
* Select mainline (explain that the releases are different git brnches?)
* Git pull Dockerfile repo from upstream
* Open and examin Dockerfile (Replace with simplified file?)
* Pull upstream base Docker image from Dockerfile
* Create fresh Dockerfile using base image from upstream Dockerfile.
* Build docker image `docker build -t nginx:local .`
* Create docker container from local image and enter container.
* Make configuration changes inside container. Then restart the container to see changes have disappeared. 
* Write script to automate changes.
* Turn script into Dockerfile sourced FROM upstream image in Repo.
* Re-build from Dockerfile and push to project registry in artifact registry.
* Cloud usage
