Return to [README](../README.md) \
Return to [skill tree](skill_tree.md)

# Linux Exercise

## Markdown

This document outlines a series of basic Linux commands you'll practice.

## Task

* **Navigate to the Home Directory:**

  Begin by navigating to your user's home directory using the `cd ~` command. This tilde symbol (`~`) represents a shortcut to your home directory.

* **Verify Current Location:**

  Use the `pwd` command to display the absolute path of your current working directory. This helps confirm you're in your home directory.

* **List Directory Contents:**

  Use the `ls` command to list the contents of the current directory, which should be your home directory at this point.

* **Create a New Directory:**

  Create a new directory named "documents" using the `mkdir documents` command.

* **Change Directory:**

  Navigate into the newly created "documents" directory using the `cd documents` command.

* **Verify Current Location (Again):**

  Use the `pwd` command again to display the absolute path of your current working directory. This time, it should show the path to the "documents" directory.

* **Create a Text File:**

  Create a new text file named "test.txt" within the "documents" directory using the `touch test.txt` command.

* **Verify File Existence:**

  Use the `ls` command again to confirm the presence of the "test.txt" file in the current directory.

* **View File Contents (Optional):**

  Use the `cat test.txt` command to display the contents of the "test.txt" file on the screen. However, `cat` doesn't work well with large files, so be cautious.

* **Copy a File:**

  Let's say you have another file called "important_data.txt" in your home directory. Use the `cp important_data.txt documents/` command to copy "important_data.txt" from your home directory to the "documents" directory. 

* **Move a File (or Rename):**

  Use the `mv test.txt another_name.txt` command to rename the "test.txt" file within the "documents" directory to "another_name.txt". Alternatively, you can use `mv` to move the file to another directory. For example, `mv another_name.txt ../` would move it back to your home directory.

* **Delete the Text File:**

  Delete the "another_name.txt" file using the `rm another_name.txt` command. Be cautious when using `rm`, as deleted files are typically unrecoverable.

* **Navigate Back to Home Directory:**

  Return to your home directory using the `cd ..` command. The double dots (`..`) represent the parent directory of the current location.

* **Delete the Directory (Optional):**

  Finally, delete the "documents" directory using the `rmdir documents` command. Remember that `rmdir` only works on empty directories; remove any files within "documents" first if necessary.

## Skills Tested

This exercise tests your understanding of:

* Basic navigation commands (cd)
* Displaying current working directory (pwd)
* Listing directory contents (ls)
* Creating directories (mkdir)
* Creating files (touch)
* Deleting files (rm)
* Deleting directories (rmdir)
* Viewing file contents (cat, optional)
* Copying files (cp)
* Moving/Renaming files (mv)

By successfully completing these tasks, you'll gain a solid foundation for working with directories and files in the Linux terminal.
