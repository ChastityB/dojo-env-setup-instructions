---
layout: page
title: “code” Command Not Working (Mac)
parent: Troubleshooting
nav_order: 3
---

# "code" Command Not Working (Mac)

![](../../images/lp/code_not_found.png)

- If you are trying to open VS Code using the "code" command in your Terminal and receive an error message that says

```
command not found: code
```

- **Open VS Code manually** (check the Applications folder or use Spotlight Search)
- Open the Command Palette.
  - On the menu bar (top of the screen), select "View" > and then select "Command Palette"

![](../../images/lp/command_palette.png)

- A popup window will appear with a ">" prompt.

![](../../images/lp/command_palette_popup.png)

- Start typing "install code" and you should see the option appear for "Shell Command: Install 'code' command in PATH".
  - Click on this option.

![](../../images/lp/install_code_command.png)

- It will then notify you that you will be prompted to give "osascript" administrative privileges.

![](../../images/lp/code_command_prompt.png)

- Click OK and then on the next pop-up window, enter your normal password for your Mac.
  - You should see a success message like the one below.

![](../../images/lp/success_code_command.png)

- You are all set! Try the code command again.

- **NOTE: if you get an error message when running the install code command:**
  - First UNinstall the code command (which is counter-intuitive).![](../../images/lp/uninstall_code.png)
  - Then rerun the install code command.
