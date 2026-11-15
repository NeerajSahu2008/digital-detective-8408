# Mission 3 — Understand the operating system

## 1. Task / objective
Explore the operating system, running processes, storage, paths and file permissions, and describe the responsibilities of an operating system.

## 2. Work completed
I used Terminal to check my operating system, account, storage and system activity, looked at the process list and PIDs, compared absolute and relative paths, read file permissions, and completed a table of OS responsibilities.

### Task 3.1 — Explore my operating system

| Information explored | What it tells you | My observation (privacy-safe) |
|----------------------|-------------------|-------------------------------|
| Operating system / system details (`sw_vers`, `uname -s`) | Which OS and version the computer is running | macOS, version YOUR_VERSION; kernel name is Darwin |
| Current account identity (`whoami`) | Which user account is currently logged in and running commands | The account name is [redacted] |
| Available and used storage (`df -h /`) | How much disk space is total, used and still free | Total YOUR_SIZE, used YOUR_USED, available YOUR_AVAILABLE |
| System activity snapshot (`top -l 1 \| head -n 10`) | A quick view of CPU use, memory use and the number of running processes | It showed how many processes were running and how busy the CPU and memory were at that moment |

### Task 3.2 — Understand processes
- **What is a process?** A process is a program that is currently running. When I open an app, the OS starts a process for it and gives it memory and CPU time.
- **What does the PID column represent?** PID is the process identifier, a unique number the OS gives to each running process so it can track and manage it.
- **Two examples of processes on my computer:** the browser I opened (for example Google Chrome or Safari) and background system processes such as `launchd` (it starts and manages other processes on macOS) or Finder.

### Task 3.3 — Paths and permissions
- **Absolute path:** the full address of a file or folder starting from the root `/`. It works from anywhere. Example from my folder: `/Users/[redacted]/digital-detective-8408/mission-03-operating-system`
- **Relative path:** an address that starts from the folder I am currently in. Example: from the repository root, `mission-03-operating-system/README.md`, or `../mission-02-terminal` from inside a mission folder.
- **What I observed:** when I used `cd mission-03-operating-system` the path shown by `pwd` got longer, and when I used `cd ..` it went back one level.

**Permissions:** I ran `ls -l` on a file in my practice area and the permissions looked like `-rw-r--r--`. The first letters after the dash belong to the owner: `rw-`.

| Permission | Meaning | Example |
|------------|---------|---------|
| r — Read | Allows a file's contents to be read | Opening a text file |
| w — Write | Allows a file to be changed | Editing a text file |
| x — Execute | Allows a file to be run; on a directory, allows access | Running a script |

In my file the owner can read and write but cannot execute, because the third letter is `-`. I did not change any permissions.

### Task 3.4 — Operating-system responsibilities

| OS responsibility | My explanation | Example |
|-------------------|----------------|---------|
| Process management | The OS decides which programs run and gives each one CPU time so many programs can run together | Browser and VS Code running at the same time |
| Memory management | The OS gives RAM to programs and takes it back when they close so programs do not interfere with each other | Closing an app frees its RAM |
| Device management | The OS controls hardware like the keyboard, screen and printer through drivers | The OS shows what I type on the screen |
| File management | The OS stores, organises, finds and protects files and folders | Creating and moving files in Finder or Terminal |
| User interface / shell | The OS gives me a way to talk to the computer, either by clicking (GUI) or typing commands (shell) | Finder and Terminal |
| Security and permissions | The OS controls who can read, change or run files and protects the system from harmful actions | A file where only the owner can write |

## 3. Commands / tools used
- `sw_vers`, `uname -s`: show the OS name and version.
- `whoami`: shows the current account (redacted in this README).
- `df -h /`: shows disk space in readable sizes.
- `top -l 1 | head -n 10`: one snapshot of system activity.
- `ps aux`: lists running processes with their PIDs.
- `grep`: filters output to find a specific process.
- `pwd`, `cd`: show and change my location.
- `ls -l`: shows detailed listing including permissions.
- Tools: Terminal (zsh), VS Code, Git.

## 4. My understanding
The operating system sits between the hardware and the programs and manages everything: running programs, memory, files, devices and security. A process is a running program and each has a unique PID. Absolute paths start from the root and work from anywhere, while relative paths start from where I am now. File permissions (r, w, x) decide what the owner and others can do with a file. This matters because it keeps the computer organised, fair to all programs, and safe.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `mission-03-operating-system/README.md` (all observations are in this file; usernames and device names redacted)

## 8. Commit details
Commit message: "Document operating system and file management"
I pushed this commit to GitHub and checked that it is visible.