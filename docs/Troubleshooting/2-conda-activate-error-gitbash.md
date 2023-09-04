---
layout: page
title: Conda Activate Error - GitBash
parent: Troubleshooting
nav_order: 2
---

# conda activate error - GitBash

## PROBLEM:

---

- You see the following error message in GitBash:

```
CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.
To initialize your shell, run
    $ conda init <shell_name>
Currently supported shells are:
  - bash
  - fish
  - tcsh
  - xonsh
  - zsh
  - powershell
See 'conda init --help' for more information and options.
```

### Solution 1:

- For your computer, run "source activate dojo-env" instead of conda activate.
  - ANYTIME you see a set of instructions that says to run "conda activate" you should ALWAYS replace the word "conda" with "source".

```
source activate dojo-env
```

### PROBLEM - V2:

- If you are seeing this message EVERY time you open a new GitBash Window.

Solution 2:

- During step 2, you were told to run the following echo conda activate command but your computer requires you to use "source activate" instead of "conda activate"

```
## INCORRECT What you ran previously
echo "conda activate dojo-env" >> ~/.bash_profile
```

- **Step 1) To fix this, you need to open the hidden file ".bash_profile" in VS Code to fix the command**.
  - In GitBash run the following command to open the file in VS Code.

```
code ~/.bash_profile
```

- **If this doesn't work and says file not found,** change the "~./" to your full file path to your user folder:

  - In the example below, replace <USERFOLDER> with your actual User account name.

    - Note: if you do not know your username, run the "whoami" command in GitBash. The text displayed is your <USERFOLDER>

```
code /c/Users/<USERFOLDER>/.bash_profile
```

- **Step 2) in the vs code window that opens, you should see the 3 lines of text below.  
  **

```
conda activate dojo-env
alias jnb="jupyter notebook"
alias lab="jupyter lab"
```

- Replace the word "conda" with "source" and then click on File > Save.

- So your final .bash_profile should now say:

```
source activate dojo-env
alias jnb="jupyter notebook"
alias lab="jupyter lab"
```

(Note: it is okay if there is additional text in this file. Whats important is that you change the conda activate command to source activate.)

- **Step 3) Open a NEW GitBash window and the message should no longer appear!**
