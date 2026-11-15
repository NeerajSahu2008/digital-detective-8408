# Mission 2 — Become comfortable with the Terminal

## 1. Task / objective
Use the command line to inspect folders, create and manage practice files, understand flags and pipes, and explain package managers.

## 2. Work completed
I practised basic Terminal operations inside my repository, did safe file changes in a `terminal-practice` folder, compared a command with and without flags, used a pipe, and checked for Homebrew.

### Task 2.1 — Basic operations

| Operation / command | What it does | What I observed |
|---------------------|--------------|-----------------|
| `pwd` | Shows the full path of the folder I am in | It printed the full path ending with `mission-02-terminal` (username [redacted]) |
| `ls` | Lists the files and folders in the current location | It showed the folders and files in the mission folder |
| `ls -l` | Lists the same items in detailed format | Each item appeared on its own line with permissions, owner, size and date |
| `cd ..` | Moves to the parent folder | My location moved one level up, to the repository root |
| `mkdir` | Creates a new folder | A new folder `practice-folder` appeared in `ls` |
| `touch` | Creates an empty file | `original.txt` was created inside the folder |
| `cp` | Copies a file to a new name | I had two files, `original.txt` and `copy.txt` |
| `mv` | Moves or renames a file | `copy.txt` was renamed to `renamed.txt`, and the old name was gone |
| `cat` | Displays the contents of a file | It printed nothing, because `original.txt` is empty |

### Task 2.2 — Safe file changes
Commands used: `mkdir terminal-practice`, `cd`, `echo "..." > notes.txt`, `echo "..." >> notes.txt`, `cat`, `cp`, `mv`, `ls`.

- **Replacing contents vs adding to the end:** `>` replaces everything in the file with the new text, so old text is lost. `>>` adds the new text at the end and keeps what was already there. I used `>` for line one and `>>` for line two, and both lines appeared.
- **Copying vs moving a file:** Copying makes a second file and keeps the original. Moving (or renaming) shifts the file to a new name or place, so the old one no longer exists.
- **What `pwd` tells me:** It shows my exact current location in the file system, so I know where my commands will act.
- **Why listing a directory is useful:** It lets me see what files and folders exist before I work with them, and check that my commands did what I expected.

### Task 2.3 — Flags and pipes
- **What changed between `ls`, `ls -l` and `ls -lah`:** Plain `ls` shows only names. `ls -l` shows one item per line with permissions, owner, size and modified date. `ls -lah` shows the same, plus hidden files (names starting with a dot) and file sizes like `4.0K` instead of raw bytes.
- **What the flags do:** `-l` = long detailed format, `-a` = show all files including hidden ones, `-h` = human-readable sizes.
- **The pipe:** The pipe `|` sends the output of the command on its left into the command on its right as input. In `ls -lah | head -n 3`, the left side creates the detailed list and the right side `head -n 3` keeps only the first three lines of it.

### Task 2.4 — Package managers
(Choose ONE, depending on your result.)

- **If Homebrew is installed:** `brew --version` showed Homebrew version X.X.X, and `brew list` showed the packages it manages.
- **If it is not installed:** `brew --version` gave "command not found", so Homebrew is not installed on my Mac. I did not install it, as the assignment said.

A package manager installs, updates and removes software from one place using simple commands. It saves time because I don't have to download and set up each tool by hand, and it keeps track of versions and dependencies so tools keep working together.

## 3. Commands / tools used
- `pwd`: shows my current folder path.
- `ls`, `ls -l`, `ls -lah`: list files, with more detail and hidden files as needed.
- `cd`: moves between folders.
- `mkdir`: creates a folder.
- `touch`: creates an empty file.
- `cp`: copies a file.
- `mv`: moves or renames a file.
- `cat`: displays a file's contents.
- `echo` with `>` and `>>`: writes text to a file, replacing or adding.
- `head`: shows the first few lines of output.
- `|` (pipe): sends one command's output to another.
- `brew --version`, `brew list`: check Homebrew.
- Tools: Terminal (zsh), VS Code, Git.

## 4. My understanding
The Terminal lets me control the computer by typing commands instead of clicking. I learned that I can move around folders, create, copy, rename and read files, and that each command does one small job. Flags change how a command behaves, like `-l` for more detail, and pipes let me chain commands so the output of one becomes the input of the next. This matters because developers use these tools to work faster and to automate tasks.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `terminal-practice/notes.txt`
- `terminal-practice/backup-notes.txt`
- `practice-folder/original.txt` and `practice-folder/renamed.txt`

## 8. Commit details
Commit message: "Complete Terminal and file management mission"
I pushed this commit to GitHub and checked that it is visible.