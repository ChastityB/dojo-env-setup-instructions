---
layout: page
title: Uninstalling Anaconda (Completely)
parent: Troubleshooting
nav_order: 7
---

# Uninstalling Anaconda (Completely)

When facing stubborn environment problems, sometimes the best course of action is to completely uninstall the environment AND Anaconda and to start over.

**Pre-Uninstallation Verification Step:**

- **If you share your computer with another User who also uses Python:**

  - Pause here and check with them BEFORE you uninstall anaconda. **You will be removing all of their python environments too,** even though they have a separate User account.

- **If you share your computer with someone and they have concerns about uninstalling anaconda:**
  - **Stop here (for now)**.
    - Do not move forward with the instructions until you have spoken with your instructor.

#### Official Steps for Fully Uninstalling Anaconda:

The following steps are taken directly from the [Official Uninstalling Anaconda documentation page](https://docs.anaconda.com/anaconda/install/uninstall/), specifically "Option B. Full uninstall using Anaconda-Clean and simple remove."

- **Install the Anaconda-Clean package from Anaconda Prompt (terminal on Linux or macOS):**

`conda install anaconda-clean`

- In the same window, run the following command:

`anaconda-clean --yes`

- Once the process has been completed, manually delete any "anaconda3" or "anaconda2" folders that still exist.
  - It may be located in one of several possible folders. Run the following "ls -a" commands until you see a folder called "anconda2" or "anaconda3".
  - **Once you see an anaconda folder, take note of:**
    - **Which command showed the folder.**
      - **Specifically, what did the command say after "ls -a"**
      - We will refer to this as your "base folder" in the final step.
    - **If the anaconda folder was "anconda2" or "anaconda3"**
      - We will refer to this as your "anaconda folder" in the final step.
  - **and j** ump to the very last command at the bottom of the page, with those 2 pieces of information.

`ls -a ~/ ls -a ~/opt/ ls -a /opt/`

- Run the final command to remove the anaconda folder once you've identified your "base folder" and "anaconda folder".
  - Replace {base_folder} with the actual folder name
  - Replace {anaconda_folder} with the actual folder name.

`rm -rf {base_folder}{anaconda_folder}`

Once you've replaced the placeholder folder names with your actual folder names, the command should look something like this:

`rm -rf ~/opt/anaconda3 # or rm -rf ~/anaconda2 # or rm -rf ~/opt/anaconda3`

####

#### Final Verification Step:

- **Now, open a new terminal window and try running the "conda" command again. Your terminal should say that conda is not found.**

  - **If it says conda is not found, you are now ready to jump back up to the "Step 3 Commands"** header above.
  - **If your computer still displays a list of conda commands** : please see the final portion of the [Official Uninstallation Instructions "Removing Anaconda from .bash_profile"](https://docs.anaconda.com/anaconda/install/uninstall/#removing-anaconda-path-from-bash-profile), which is illustrated below:

- **Open the two settings file for your terminal and remove anything related to anaconda:**
  _ **1) Run the "open ~/.bash_profile" (without quotation marks) command and a text editor window should open.**
  _ Examine the contents of this file and **delete any lines that look like either of the screenshots below** :
  _  
  ![](../../images/lp/conda_init_code.png)
  _ ![](../../images/lp/Screen_Shot_2022-08-05_at_6.55.05_PM.png)
  _ Save the file and close it.
  _ 2) **Now repeat the process, but use the "open ~/.zshrc"** (without quotation marks) command
  _ Delete any lines of code that look like the screenshots above.
  _ Save the file and close it.

- **FInal Verification:**

  - Open a New Terminal Window (the changes you made above only take effect when opening a new window)
  - Run the "conda" command again and you should now see a message that says "conda not found"
    - If you are still seeing the list of conda commands instead, re-open the two files listed above and make sure you saved them after deleting the lines of code.
    - Close your terminal window and open a new one and try the "conda" command again.

- **If the conda command still displays the list of commands after the steps above:**
  - **Try restarting your computer** and attempting to run the command one more time.
  - **If you are still seeing conda commands:**
    - You should post your problem on the [ds-python-installation](https://discord.com/channels/738494436467539968/999108307627294770) discord channel for a TA or instructor to assist you.
    - You can also email your instructor about the issue (please cc: jirving@codingdojo.com)
