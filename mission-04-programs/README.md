# Mission 4 — How programs run

## 1. Task / objective
Run a simple Python program and compare how compilers and interpreters translate or execute programs.

## 2. Work completed
I created a Python file named `hello.py` in this folder that prints "Hello from Python", ran it from Terminal using Python 3, and confirmed the message appeared. I also compared a compiler and an interpreter in a table and explained the difference.

### Task 4.1 — Create and run a Python program
The program in `hello.py` is one line:

    print("Hello from Python")

I ran it with `python3 hello.py` and the output was:

    Hello from Python

### Task 4.2 — Compare compiler and interpreter

| Point | Compiler | Interpreter |
|-------|----------|-------------|
| When translation / execution happens | The whole program is translated before it runs | The program is read and executed while it runs, one instruction at a time |
| Typical output | A separate executable or machine-code file | No separate file; the program's results appear directly |
| One example | C compiled with `gcc` | Python run with `python3` |
| One advantage | The finished program usually runs faster | It is quick to test and change code, and errors show up as soon as that line runs |

**Explanation:** A compiler translates the entire source code into machine code first, and then I run the translated program. An interpreter does not make a separate file. It reads my code and carries out the instructions while the program is running. Compiled programs usually run faster, while interpreted programs are easier to test because I can change the code and run it again immediately. Real languages can mix both ideas. For example, Python first converts code into a simpler internal form and then runs that.

## 3. Commands / tools used
- `cd`: moves into the mission folder.
- `echo` with `>`: writes the line of code into `hello.py`.
- `python3 hello.py`: runs the Python program using the Python 3 interpreter.
- `cat`: displays the contents of `hello.py` to check it.
- Tools: Terminal (zsh), VS Code, Git.

## 4. My understanding
A program written in a language like Python or C is just text, and the computer cannot run it directly. It has to be translated into instructions the processor understands. A compiler does this translation before the program runs, and an interpreter does it while the program runs. This matters because it explains why compiled programs are often faster, and why Python feels easy to test and quick to change.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `mission-04-programs/hello.py`
- `mission-04-programs/README.md` (output and comparison are in this file)

## 8. Commit details
Commit message: "Compare compilers and interpreters"
I pushed this commit to GitHub and checked that it is visible.