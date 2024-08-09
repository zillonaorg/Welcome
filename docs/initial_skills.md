# Initial Skills

Get started by setting up your development environment and contributing to the 
Zillona Org documentation project.

## Create Linux Virtual Machine

**Access a Debian Virtual Machine**

## Install Packages and Configure Linux Environment

  * vim
  * git
  * mkdocs
  * docker
  * Nginx
  * Docker Engine
  * configure

## Save the Commands

**Save the Previous Steps to a Bash File**

## Contribute to the Documentation Project

Zillona Org documentation is publicly viewable at 
[https://zillonaorg.github.io](https://zillonaorg.github.io) 
or
[https://docs.zillona.org](https://docs.zillona.org/)

The HTML is hosted via GitHub from the publishing repository at
[github.com/zillonaorg/zillonaorg.github.io](https://github.com/zillonaorg/zillonaorg.github.io) 

To make changes to the code

**Pull the Documentation Source Repository**

The Markdown source for the documentation project can be found at
[github.com/zillonaorg/Welcome](https://github.com/zillonaorg/Welcome)

To contribute to the documentation project clone the source repository, change
directory into the local git clone and create a new branch from the "develop"
branch.

```
git clone https://github.com/zillonaorg/Welcome.git
cd ./Welcome/
git checkout develop
git pull
git checkout -b YOUR_BRANCH_NAME
```

**Edit the Markdown Files with Your Changes**

Open another shell/terminal and change directory into your local git clone
again. From the root of your local repo where you find the mkdocs.yml file, run
the MkDocs server to render your Markdown files as HTML locally. 

```
cd Welcome
mkdocs serve
```

You _may_ have to prepend your mkdocs command with `python -m ` as follows 

```
python -m mkdocks serve
``` 

The MkDocs server will continue to run in the foreground of the terminal
outputting logs as you make your changes. Return to your other terminal to
continue with your local development.

While the server is running you can view your changes, rendered as HTML code in 
real time by visiting [http://localhost:8000/](http://localhost:8000/) in your 
browser.
                                                                                 
Please reference this 
[cheat sheet](https://www.markdownguide.org/cheat-sheet/) from 
[makeareadme.com](https://www.makeareadme.com/) and the official GitHub Markdown
[style guide](https://google.github.io/styleguide/docguide/style.html) when 
editing the Markdown files.

**Share Your Changes**

To contribute back to the documentation project and share your changes you will
need to use git commands to add, commit and push your local changes back to
GitHub.

```
git add CHANGED_FILE_NAME
git commit
git push --set-upstream origin YOUR_BRANCH_NAME
```

**Create a Pull Request**

Merge your branch back into the develop branch.

**Publish Your Changes Publicly**

Once your changes along with all other changes to the develop branch have been
validated a pull request against the main branch will be created to deploy a 
"release" of the public [documentation website](https://zillonaorg.github.io). 

Once the develop branch has been merged to main we can create the HTML website
from the main branch using MkDocs.

Once again the mkdocs command must be ran from the root of your git repository.

```
mkdocs build -s
```

Again, you _may_ have to prepend your mkdocs command with `python -m ` as follows 

```
python -m mkdocks build -s
``` 

MkDocs will convert the Markdown files inside the /docs directory into an MkDocs
HTML website stored in a new /site directory created by the build process.

The resulting website "artifact" is ready for deployment to any webserver. We
host our documentation website in GitHub at 
[https://zillonaorg.github.io](https://zillonaorg.github.io/). 

Deployment is achieved by pushing the website artifact changes to 
[github.com/zillonaorg/zillonaorg.github.io](https://github.com/zillonaorg/zillonaorg.github.io) 
and merging to the main branch.
