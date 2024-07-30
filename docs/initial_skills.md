# Initial Skills

Get started by setting up your development environment and contributing to the 
Zillona Org documentation project.

## Install Debian VM

## Install Necessary Packages

  * mkdocs
  * git
  * docker
  * vim

## Contribute to the Documentation Project

Zillona Org documentation is publicly viewable at 
[https://zillonaorg.github.io](https://zillonaorg.github.io) 
or
[https://docs.zillona.org](https://docs.zillona.org/)

The HTML is hosted via GitHub from the publishing repository at
[github.com/zillonaorg/zillonaorg.github.io](https://github.com/zillonaorg/zillonaorg.github.io) 

**Pull the Documentation Source Repository**

The Markdown source for the documentation project can be found at
[github.com/zillonaorg/Welcome](https://github.com/zillonaorg/Welcome)

To contribute to the documentation project pull the source repository, change
directory into the local git clone and create a new branch from the "develop"
branch.

```
git clone https://github.com/zillonaorg/Welcome.git
cd ./Welcome/
git checkout develop
git checkout -b YOUR_BRANCH_NAME
```

**Edit the Markdown Files with Your Changes**
                                                                                 
Please reference this 
[cheat sheet](https://www.markdownguide.org/cheat-sheet/) from 
[makeareadme.com](https://www.makeareadme.com/) and the official GitHub Markdown
[style guide](https://google.github.io/styleguide/docguide/style.html) when 
editing.

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

## Install Nginx

## Install Docker Engine
                                                                                 
