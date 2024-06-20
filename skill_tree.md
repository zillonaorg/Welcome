Return to [README.md] (README.md)

# Proposed skill tree progression

## Pre-Requisites:

* Navigate Linux filesystem
* Edit local files
* Basic git usage.

## First steps: "Getting Padawan'd in"

* Have them install a local Debian VM on their workstation.
* Vim? ("Stateful" editing / editing modes) (( `:w` is `git commit`, `:q` is `git push` ))
* Install cli tools and dependencies packages (Vim, git, curl, etc)
* Create change branch from "dev"and edit Markdown README.md file in Welcome repo 
* Add, commit, push and merge changes to dev and validate changes
* HTML editing
* Install nginx in the VM
* Bash scripting (Save install steps)
* Configure nginx from the CLI
* Install Docker on the VM

## Next steps:

Docker:
* https://hub.docker.com/_/nginx
* Select mainline (explain that the releases are different git brnches?)
* Git pull Dockerfile repo from upstream
* Open and examin Dockerfile (Replace with simplified file?)
* Build docker image `docker build -t nginx:local .`
* Create docker container from local image and enter container.
* Make configuration changes inside container. Then restart the container to see changes have disappeared. 
* Write script to automate changes.
* Turn script into Dockerfile sourced FROM upstream image in Repo.
* Re-build from Dockerfile and push to project registry in artifact registry.
* Cloud usage

## Building core skills:

* Advanced git (Branching strategies, Merging strategies, Fixing mistakes)
* Advanced Linux skills
* Advanced Nginx (or other service configuration)

## Advanced topics:

* Cloud administration
* Network fundamentals
* Kubernetes: (Administration)
**  Installation
**  Configuration
**  Usage
* TF Code / Ansible
* Programming
* Release cycles
* pipelines

