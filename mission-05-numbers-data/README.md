# Mission 5 — Numbers and data

## 1. Task / objective
Convert decimal, binary and hexadecimal values, verify results with Python, build a small converter program and explain how text is stored.

## 2. Work completed
I converted numbers by hand and showed my working, checked each answer in the Python interactive shell, wrote `number_converter.py`, tested it with three numbers, and answered questions about text encoding.

### Task 5.1 — Manual conversions

| Question | My working and answer |
|----------|-----------------------|
| Decimal 13 to binary | 13 ÷ 2 = 6 remainder 1; 6 ÷ 2 = 3 remainder 0; 3 ÷ 2 = 1 remainder 1; 1 ÷ 2 = 0 remainder 1. Reading remainders from bottom to top: **1101** |
| Decimal 25 to binary | 25 ÷ 2 = 12 r 1; 12 ÷ 2 = 6 r 0; 6 ÷ 2 = 3 r 0; 3 ÷ 2 = 1 r 1; 1 ÷ 2 = 0 r 1. Reading bottom to top: **11001** |
| Binary 1010 to decimal | (1×8) + (0×4) + (1×2) + (0×1) = 8 + 0 + 2 + 0 = **10** |
| Binary 1101 to decimal | (1×8) + (1×4) + (0×2) + (1×1) = 8 + 4 + 0 + 1 = **13** |
| Hexadecimal A to decimal | A stands for 10, so the answer is **10** |
| Hexadecimal 1F to decimal | (1×16) + (F×1) = 16 + 15 = **31** |
| Binary 1111 to hexadecimal | 1111 = 8 + 4 + 2 + 1 = 15, and 15 is F in hexadecimal, so the answer is **F** |

### Task 5.2 — Verification using Python

| Expression tested | Python result | Matches my manual answer? |
|-------------------|---------------|---------------------------|
| `bin(13)` | `0b1101` | Yes (1101) |
| `bin(25)` | `0b11001` | Yes (11001) |
| `int("1010", 2)` | `10` | Yes |
| `int("1101", 2)` | `13` | Yes |
| `hex(25)` | `0x19` | Yes (25 = 16 + 9, so 19 in hex) |
| `hex(31)` | `0x1f` | Yes (31 is 1F in hex) |
| `int("A", 16)` | `10` | Yes |
| `int("1F", 16)` | `31` | Yes |
| `hex(int("1111", 2))` | `0xf` | Yes (F) |

The `0b` at the start means the number is binary and `0x` means it is hexadecimal. They are only labels and not part of the value.

### Task 5.3 — Number converter

The program in `number_converter.py`:

    number = int(input("Enter a decimal number: "))

    print("Decimal:", number)
    print("Binary:", bin(number))
    print("Hexadecimal:", hex(number))

**How it works:** `input()` asks the user to type something, but it always gives back text. `int()` changes that text into a whole number. `bin()` converts the number to a binary string and `hex()` converts it to a hexadecimal string. `print()` shows the results.

**How to run it:**

    python3 number_converter.py

| Test number | Binary output | Hexadecimal output |
|-------------|---------------|--------------------|
| 10 | 0b1010 | 0xa |
| 25 | 0b11001 | 0x19 |
| 255 | 0b11111111 | 0xff |

### Task 5.4 — How is text stored?
- **ASCII codes:** uppercase A = 65 and lowercase a = 97 (checked with `ord("A")` and `ord("a")`).
- **Why an encoding standard is needed:** A computer can only store numbers (bits), so each character has to be given a number. An encoding standard makes sure every computer uses the same number for the same character, so text looks the same everywhere.
- **A character not in basic ASCII:** the rupee sign ₹ (also é or emoji).

## 3. Commands / tools used
- `python3`: opens the Python interactive shell.
- `bin()`: converts a decimal number to a binary string.
- `hex()`: converts a decimal number to a hexadecimal string.
- `int(text, base)`: converts text in binary (base 2) or hexadecimal (base 16) to a decimal number.
- `int()`: converts typed text to a whole number.
- `input()`: reads what the user types.
- `print()`: displays results.
- `ord()`: gives the code number of a character.
- `python3 number_converter.py`: runs my program.
- Tools: Terminal (zsh), VS Code, Git.

## 4. My understanding
Computers store everything as bits, which are 0 or 1, and 8 bits make a byte. Decimal is base 10, binary is base 2 and hexadecimal is base 16. I learned to convert by dividing by 2 and reading remainders upward, and to convert back using place values. Hexadecimal is useful because one hex digit represents four bits, so long binary numbers become short. Text is stored using encoding standards like ASCII and UTF-8, where each character has a number. This matters because it shows how all data, numbers and text, becomes bits inside a computer.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
- `mission-05-numbers-data/number_converter.py`
- `mission-05-numbers-data/README.md` (manual working, Python verification, test results and encoding answers)

## 8. Commit details
Commit message: "Build number converter and practise data representation"
I pushed this commit to GitHub and checked that it is visible.