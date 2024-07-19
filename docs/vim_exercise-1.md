# Using the Vim Editor in Linux

## Get hands-on with VIM

This exercise will guide you through basic VIM commands for editing text files.

### Task

* **Create a File:**

  Open a terminal and navigate to your desired directory. Create a new file named `practice.txt` using VIM: `vim practice.txt`

* **Enter Insert Mode:**

  Press the `i` key to enter insert mode. Notice the `-- INSERT --` indicator at the bottom of the screen. Type a few sentences or lines of text.

* **Exit Insert Mode:**

  Press the `Esc` key to exit insert mode.

* **Navigation:**

  Use the arrow keys to move the cursor around the text. Try these commands for faster navigation:
  * `h` (left), `j` (down), `k` (up), `l` (right)
  * `w` (next word), `b` (previous word)
  * `0` (beginning of line), `$` (end of line)

* **Editing:**

  * **Deleting:**
    * `x` deletes the character under the cursor.
    * `dw` deletes a word.
    * `dd` deletes an entire line.
  * **Copying/Pasting:**
    * `yy` copies (yanks) a line.
    * `p` pastes the copied content below the current line.
  * **Undo/Redo:**
    * `u` undoes the last action.
    * `Ctrl-r` redoes the last undone action.

* **Saving and Exiting:**

  * **Saving:**
    * Type `:w` and press Enter to save the changes.
  * **Exiting:**
    * Type `:q` and press Enter to quit VIM if you've saved changes.
    * Type `:q!` and press Enter to quit without saving changes.

### Skills Practiced

This exercise introduces you to:

* Opening and creating files with VIM
* Entering and exiting insert mode
* Basic navigation commands
* Essential editing commands (deleting, copying, pasting, undo/redo)
* Saving and exiting VIM

By practicing these commands, you'll start building a foundation for efficient text editing in VIM.


### Official Resources

* **Documentation:**
  * Vim User Manual: This is the comprehensive reference for all Vim features. Unfortunately, there's no single, direct link to it, as it's integrated into the Vim editor itself. To access it, open Vim and type `:help` followed by the specific topic you want to explore (e.g., `:help insert`).

### Third-Party Resources
* Tutorials and Examples:
  * Vim Tutorial: While not officially endorsed, this tutorial provides a good starting point: https://www.freecodecamp.org/news/vim-beginners-guide/
  * Learn Vimscript the Hard Way: This book offers a deep dive into Vim scripting: https://github.com/yuchao86/Learn-Vimscript-the-Hard-Way
  * Open Vim: A web-based interactive Vim tutorial: https://opensource.com/article/19/3/getting-started-vim
* Note: Due to the nature of Vim, there might not be specific style guides or certifications associated with it. The community primarily relies on the extensive documentation and user-created resources.

