# Zillona Org

This repository is home to the documentation source for Zillona Org, the Zillona
Dojo and associated projects.

We generate the organizations documentation site https://zillonaorg.github.io 
from this source using mkdocs.

Read the [docs](https://zillonaorg.github.io)

## Getting started

Please see our [contributing guide](https://zillonaorg.github.io/contributing/)

Clone this repository 

`git clone https://github.com/zillonaorg/Welcome.git`

`cd ./Welcome`

Make a new branch for your work where _<new_branch>_ is your new branch name.

`git checkout -b <new_branch> --track develop`

If you need git help, please see our 
[beginners git exercise](https://zillonaorg.github.io/git_exercise-1/)

This project uses Markdown language for documentation formatting.

Refer to [markdownguide.org](https://www.markdownguide.org/) for basic syntax 
and a cheat sheet for your quick reference.

Please reference the official GitHub Markdown 
[style guide](https://google.github.io/styleguide/docguide/style.html) 
when editing.

Install [mkdocs](https://www.mkdocs.org/)

  * Using the Debian package repositories

`sudo apt install mkdocs`

  * With pip

`pip3 install mkdocs`

In another terminal run mkdocs server inside your git checkout. Navigate to your
local copy of the repository in a new terminal and run the mkdocs web server to
tail live logs of server events.

`mkdocs serve`

Go to [localhost](http://127.0.0.1:8000) in your browser to view your website in 
real-time while you edit

When you are happy with your contribution add, commit and push your changes to 
this repository and create a 
[pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
to merge to the develop branch.
