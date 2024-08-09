# Beginners Git Lifecycle Exercise

### Get hands on with Git

This exercise will guide you through basic Git commands for version control.

### Task

* **Clone a Repository:**

  Find a repository on GitHub you'd like to work with. Copy its HTTPS URL. In your terminal, navigate to where you want to store the project and run: `git clone <repository_url>`

* **Create a New Branch:**

  It's good practice to create a new branch for your work. Navigate into the cloned repository: `cd <repository_name>`. Then create a branch: `git checkout -b <new_branch_name>`. (If theres an existing branch, you can switch to it using: `git checkout <existing_branch_name>`.)

* **Make Changes:**

  Open the project files in your code editor and make some modifications. Save your changes.

* **Stage Changes:**

  Tell Git to track your changes: `git add <file_name>` (for specific files) or `git add .` (to stage all changes).

* **Commit Changes:**

  Record your changes with a descriptive message: `git commit -m "Your commit message here"`

* **Push Changes:**

  Send your committed changes to the remote repository (GitHub): `git push origin <new_branch_name>`

### Skills Practiced

This exercise introduces you to:

* Cloning a repository (`git clone`)
* Creating a new branch (`git checkout -b`)
* Staging changes (`git add`)
* Committing changes (`git commit -m`)
* Pushing changes to a remote repository (`git push`)

By practicing these commands, you'll start building a foundation for version control and collaboration using Git.
