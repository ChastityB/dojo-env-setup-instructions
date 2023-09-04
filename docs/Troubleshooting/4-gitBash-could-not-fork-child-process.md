---
layout: page
title: "GitBash Error: Could Not Fork Child Process"
parent: Troubleshooting
nav_order: 4
---

# GitBash Error: Could Not Fork Child Process

## The Problem:

## Opening a GitBash windows displays an error message "Could not fork child process"

![enter image description here](https://i.stack.imgur.com/Tps5X.png)

## The Solution

**Solution 1:** (adapted from: <https://rotadev.com/git-bash-error-could-not-fork-child-process-there-are-no-available-terminals-1-dev/> )

- The problem occurs on Windows with Git Bash when the Git Bash console is closed/killed without using ‘exit’.
  - 1\. Close all Git Bash windows.
  - 2\. Open Task manager (Keyboard shortcut: Control + Shift + Escape.)
  - 3\. Find the ‘Git for Windows’ process.
    - If you do not see any "Git for Windows" processes, look for:
      - python
      - msys2
  - 4\. Kill any processes that are running that meet the above criterion.
  - 5\. Re-open Git Bash. The problem should be fixed.
  - See the Prevention heading below for how to avoid this error in the future

**Solution 2 (if #1 did not resolve the issue):**

- The problem may also occur due to VS Code's integrated terminal.
- Close any Visual Studio Code windows
- Check Task Manager for any Visual Studio Code processes that are still running and kill them.
- Re-open Git Bash. The problem should be fixed.
- See the Prevention heading below for how to avoid this error in the future

**Solution 3 (will always work but not convenient)**

- If neither solution worked, restart your computer.
- While not convenient, it will solve the issue. See the Prevention heading below for how to avoid this error in the future.

## Prevention

- Always make sure to shut down jupyter notebook properly before closing.
  - From jupyter's file view:
    - Click Shutdown on the top right corner
  - From GitBash:
    - Press "Control + C" to quit jupyter server from the GitBash window that started jupyter notebook.
      - If asked y/n, answer "y".
