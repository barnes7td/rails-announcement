# Sublime Tip \#1

This tip we are going to discuss some Setup. 

---

**Setting up Sublime for the command line**

It is useful to open up Sublime from the command line. We want to setup the command ``subl`` to open up Sublime. Once setup, the command ``subl .`` will open up the current directory. the command ``subl program.rb`` will open up the ``program.rb`` file. Here is how you set it up:

Mac/Linux: 

1. Make sure you have a directory call ``~/bin``. If not create the directory with: ``mkdir ~/bin``

1. Symlink the sublime executable to your ``~/bin`` directory: ``ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl``

1. Make sure the ``~/bin`` directory is in your PATH: ``echo 'export PATH=$PATH:$HOME/bin' >> ~/.bash_profile`` Note: the ``~/.bash_profile`` file is used for adding your customizations to a bash terminal (default on OSX and Linux). However, if you are using another shell like zsh, use the appropriate config file.

Windows (Git Bash):

1. Windows by default should open up Sublime Text 2 at the command with the command ``sublime_text``, However if you would prefer the shorter ``subl`` command, then create a file called ``.bash_profile`` (or open an already created file) and type the line ``alias subl='"/c/Program Files/Sublime Text 2/sublime_text.exe"'``. After restarting Git Bash the ``subl`` command should work.

Windows (CMD):

1. Make sure ``C:\Program Files\Sublime Text 2`` in your PATH. [How to add directory to Window's PATH](http://www.computerhope.com/issues/ch000549.htm). Make sure that there is a semi-colon ``;`` between each directory in the path.

1. Create a new file and save it as ``subl.bat`` in the directory ``C:\Program Files\Sublime Text 2``

1. Inside the ``subl.bat`` file put the line: ``start sublime_text.exe %*``. After restarting CMD the ``subl`` command should work.

---

**Setting up Sublime as the default editor**

This is important for when you type the line ``git commit`` without the ``-m`` option. By default this will open up terminal vim, which is confusing if you have never seen before. If you get stuck in vim the command ``:q`` will exit vim.  To instead open up Sublime:

Mac/Linux:

1. Type ``echo "export EDITOR='subl -w '" >> ~/.bash_profile`` at the command line. Remember use the appropriate config file for you setup. Or manually add the line ``export EDITOR='subl -w '`` to your config file (``~/.bash_profile``).

Windows (Git Bash) and (CMD):

1. In windows we need to change the default git editor by type ``git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe'"`` at the command line.

---

**Duplicate Line Shortcut**

I want to leave you with one key shortcut to practice this week. This is the "duplicate line" command. This command simply copies the current line that your cursor is on and pastes the line on the line below your cursor. 

Mac: ``cmd + shift + D``

Win/Linux: ``ctrl + shift + D``
