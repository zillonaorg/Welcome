# Zillona Org

This repository is home to the documentation source for 
[Zillona Org](https://www.zillona.org/) as well as the 
[Zillona Dojo](https://dojo.zillona.org/) and associated projects.

We generate the organization's documentation site 
[zillonaorg.github.io](https://zillonaorg.github.io) from this source repository 
using [mkdocs](https://www.mkdocs.org/).

Read the [docs](https://zillonaorg.github.io)

## Getting started

Please see our [contributing](https://zillonaorg.github.io/contributing/) guide

Install [mkdocs](https://www.mkdocs.org/) from either the Debian package 
repositories

```
sudo apt install mkdocs
```

or via pip

```
pip3 install mkdocs
```

This project uses Markdown language for documentation formatting.

Refer to [markdownguide.org](https://www.markdownguide.org/) for basic syntax 
and a cheat sheet for your quick reference.

Please reference the official GitHub Markdown 
[style guide](https://google.github.io/styleguide/docguide/style.html) 
when editing.

## Check out the code

Check out both this repository as well as the zillonaorg.github.io publishing
[repository](https://github.com/zillonaorg/zillonaorg.github.io) in the same 
working directory and follow the steps below.

```
git clone https://github.com/zillonaorg/zillonaorg.github.io.git
```

```
git clone https://github.com/zillonaorg/Welcome.git
```

Change directory into the source repository

```
cd ./Welcome
```

Make a new branch for your work where _<new_branch>_ is your new branch name.

```
git checkout -b <new_branch> --track develop
```

If you need git help, please see our 
[beginners git exercise](https://zillonaorg.github.io/git_exercise-1/)

## Run the Development Server

Navigate to your local copy of the source repository in a new terminal and run 
the mkdocs dev server to view live logs of server events.

```
mkdocs serve
```

Go to [localhost](http://127.0.0.1:8000) in your browser to view your website in 
real-time while you edit.

Complete your changes in the source repository and validate those changes
through the website in your local dev server.

When you are happy with your contribution add, commit and push your changes to 
this repository and create a 
[pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
to merge to the _develop_ branch.

## Deploy Changes to Documentation Website

Once the _develop_ branch has been merged into the _main_ branch it is time to 
publish our changes to the public documentation website.

Build the website from inside the _main_ branch of the source repository using
mkdocs.

```
mkdocs build -s
```

You now have the generated HTML, CSS and Javascript code in the _site/_
directory

Change directory back into the publishing repository

```
cd ../zillonaorg.github.io/
```

Pull changes from remote and change into _develop_ branch

```
git pull
git checkout develop
```

Copy the contents of the site/ directory to the root of the publishing repo.

```
cp -r ../Welcome/site/* .
```

Add, commit and push your changes to the _develop_ branch for validation and
testing then submit a pull request to have your changes merged to _main_.

Once merged into _main_ your changes have been published and can be viewed at
[zillonaorg.github.io](https://zillonaorg.github.io/)).
