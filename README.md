# DR.Typing-game-using-C
C program project demonstrating C leaning and concepts and developing a fun typing game which we can play with friends.

-----

<p align="center">
  <a href="https://drive.google.com/file/d/1RK-DvmUApOqZc_9z16wl9WUM5Jk4p5rW/view?usp=sharing" target="_blank">
    <img src="https://img.shields.io/badge/📂%20View-Project%20Resource-0A66C2?style=for-the-badge&logo=google-drive&logoColor=white" />
  </a>
</p>


-----

# 🖮 DR.Typing — Offline Typing Speed Challenge

<div align="center">

```
+================================================================================+
|                        Welcome to DR.Typing                                    |
|              An offline typing speed challenge                                 |
|              where you can race against friends                                |
|              or go solo to break records!                                      |
+================================================================================+
|                        ~ Created By: Debadatta Rout ~                         |
+================================================================================+
```

![Language](https://img.shields.io/badge/Language-C-blue?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

</div>

---

## 📌 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Screens & UI Preview](#-screens--ui-preview)
- [How to Compile & Run](#-how-to-compile--run)
- [Project Structure](#-project-structure)
- [C Concepts & Knowledge Used](#-c-concepts--knowledge-used)
- [How This Game Was Built Using College-Level C Knowledge](#-how-this-game-was-built-using-college-level-c-knowledge)
- [Data Structures Used](#-data-structures-used)
- [File Handling in Detail](#-file-handling-in-detail)
- [Game Logic Explained](#-game-logic-explained)
- [WPM & Accuracy Formula](#-wpm--accuracy-formula)
- [Key Functions Reference](#-key-functions-reference)
- [Known Limitations](#-known-limitations)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 📖 About the Project

**DR.Typing** is a fully offline, terminal-based typing speed game built in **pure C language**. It was developed as a learning project to combine fundamental C programming concepts with a real, playable application that friends can use together on the same machine.

The project simulates the experience of popular online typing platforms like **MonkeyType** and **TypeRacer** — but entirely in the Windows terminal, with zero internet dependency.

> This project proves that with just **college-level C knowledge**, you can build a complete, functional, multi-user application with file persistence, scoring, rankings, and a styled terminal UI.

---

## ✨ Features

| Feature | Description |
|---|---|
| 👤 Multi-user Login | Register and login with username & password |
| ⏱️ 5 Test Durations | 15s, 30s, 50s, 120s, 150s timed typing tests |
| 📦 Word-Wrapped Text Box | Long texts auto-wrap inside a fixed-width terminal box |
| 📊 Detailed Results | WPM, Raw WPM, Accuracy, Mistakes, Consistency |
| 🏆 Global Scoreboard | Top 10 players ranked by WPM with medal symbols |
| 📁 Personal Records | Every test you take is saved and displayed in a table |
| 💾 File Persistence | Users and scores are saved to `.txt` files between sessions |
| 🎨 Terminal UI Design | Stylised borders, headings, and `.:*~*:.` decorative symbols |
| 🔐 Simple Authentication | Username + password login with duplicate user detection |
| 📝 Random Text Selection | A random passage is selected each test from a pool of 10 |

---

## 🖥️ Screens & UI Preview

### Welcome Screen
```
+================================================================================+
|                        Welcome to DR.Typing                                    |
|                        ~ Created By: Debadatta Rout ~                         |
+================================================================================+
 _________________________________________________
| 1. Existing user -----> Login                   |
| 2. New user --------> Register                  |
|_________________________________________________|
```

### Main Menu
```
 .:*~*:._.:*~*:._.:*~*:._.:*~*:._.:*~*:._.:*~*:.
 |          DR.Typing  -  Main Menu               |
 |          Welcome,  Debadatta                   |
 .:*~*:._.:*~*:._.:*~*:._.:*~*:._.:*~*:._.:*~*:.
    ..: 1.  Start Typing Test      :..
    ..: 2.  View Scoreboard        :..
    ..: 3.  View Personal Records  :..
```

### Typing Test
```
+--------------------------------------------------------------------------------+
| The greatest glory in living lies not in never falling, but in rising every   |
| time we fall. Life is what happens when you're busy making other plans.       |
+--------------------------------------------------------------------------------+
  [ 38 sec left]  > The greatest glory in living lies not in never_
```

### Results Screen
```
  +------------------------------------------------+
  |  Words Per Minute    :  57                     |
  |  Accuracy            :  89.93 %                |
  |  Consistency         :  96.79 %                |
  +------------------------------------------------+
  Performance: .:* Expert Typist *:.
```

### Scoreboard
```
  +------+------------------+-------+----------+-------+-------+----------+
  | Rank | Username         |  WPM  | Accuracy | Err   | Chars | Consist  |
  +------+------------------+-------+----------+-------+-------+----------+
  | .:1 1| Debadatta        |    82 |     96 % |     5 |   430 |   98.2 % |
  | .:2 2| Rohit            |    74 |     91 % |    11 |   391 |   94.1 % |
```

---

## ⚙️ How to Compile & Run

### Requirements
- Windows OS (uses `<windows.h>`, `<conio.h>`, and `system("cls")`)
- GCC compiler (MinGW recommended) or any C compiler (Dev-C++, Code::Blocks, Visual Studio)

### Compile with GCC (Command Prompt)

```bash
gcc dr_typing.c -o dr_typing.exe
```

### Run

```bash
dr_typing.exe
```

### Compile with Dev-C++ or Code::Blocks
1. Open the `.c` file in your IDE
2. Click **Compile & Run** (F11 in Dev-C++)
3. The program will auto-create all required `.txt` files on first run

> **Note:** All text files (`text_15.txt`, `text_30.txt`, `text_50.txt`, `text_120.txt`, `text_150.txt`, `users.txt`, `records.txt`) are created automatically in the same directory as the `.exe`.

---

## 📁 Project Structure

```
dr_typing/
│
├── dr_typing.c          ← Main source file (all code)
│
├── users.txt            ← Auto-created: stores registered users
├── records.txt          ← Auto-created: stores all test scores
│
├── text_15.txt          ← Auto-created: text passages for 15s test
├── text_30.txt          ← Auto-created: text passages for 30s test
├── text_50.txt          ← Auto-created: text passages for 50s test
├── text_120.txt         ← Auto-created: text passages for 120s test
├── text_150.txt         ← Auto-created: text passages for 150s test
│
└── README.md            ← This file
```

---

## 📚 C Concepts & Knowledge Used

This project was built using core C programming concepts taught in most undergraduate Computer Science courses. Here is a breakdown of every concept used and where:

---

### 1. 📦 `struct` — Structures (Custom Data Types)

Two custom structs form the backbone of this program:

```c
typedef struct {
    char username[50];
    char password[50];
} User;

typedef struct {
    char username[50];
    int  wpm;
    int  accuracy;
    int  mistakes;
    int  raw;
    int  charsTyped;
    float consistency;
    time_t date;
} ScoreRecord;
```

**What it teaches:**
- How to group related data under one named type
- How `typedef` eliminates the need to write `struct` every time
- How arrays of structs act like a simple in-memory database (`User users[100]`)

---

### 2. 📂 File I/O — `fopen`, `fscanf`, `fprintf`, `fclose`

The entire persistence system (saving/loading users and scores) is built with C file I/O:

```c
// Writing
FILE *f = fopen("users.txt", "w");
fprintf(f, "%s %s\n", users[i].username, users[i].password);
fclose(f);

// Reading
FILE *f = fopen("users.txt", "r");
while (fscanf(f, "%49s %49s", username, password) == 2) {
    // load into array
}
fclose(f);
```

**What it teaches:**
- Opening files in read (`"r"`), write (`"w"`), and append (`"a"`) modes
- Formatted reading with `fscanf` (returns number of items matched)
- Safe reading with `fgets` for strings with spaces
- The importance of `fclose` to flush buffers and prevent data loss
- Checking if a file already exists before creating it

---

### 3. 🔡 Strings — `string.h` Library

Strings are used everywhere — usernames, passwords, the typed text, the target text:

```c
#include <string.h>

strcpy(currentUser, username);         // copy a string
strcmp(input, users[i].username);      // compare strings
strlen(line);                           // length of a string
strcspn(username, "\n") = 0;           // strip newline character
strncpy(buf, text, MAX_TEXT_LENGTH-1); // safe bounded copy
strcat(line, " ");                      // concatenate strings
strtok(buf, " ");                       // tokenise (split) a string by delimiter
```

**What it teaches:**
- Why C strings are just `char` arrays terminated by `'\0'`
- The danger of buffer overflows — and how `strncpy` and bounds checking prevent them
- How `strtok` is used for parsing/word-wrapping text
- Why `strcmp` returns 0 for equality (not 1 like `==` would for integers)

---

### 4. ⌨️ `conio.h` — Non-Blocking Keyboard Input

The real-time typing loop uses `conio.h` functions that are Windows-specific:

```c
#include <conio.h>

if (_kbhit()) {          // returns 1 if a key is waiting in the buffer
    char c = _getch();   // reads one character without waiting for Enter
}
```

**What it teaches:**
- The difference between **blocking** (`scanf`, `getchar`) and **non-blocking** input
- How games and real-time applications read input without pausing execution
- The role of the keyboard buffer in the OS

---

### 5. ⏰ Time Functions — `time.h`

Time is used both for the typing test countdown and for timestamping scores:

```c
#include <time.h>

time_t startTime = time(NULL);          // get current Unix timestamp
time_t endTime   = startTime + 50;      // add seconds

while (time(NULL) < endTime) {          // real-time countdown loop
    long remaining = endTime - time(NULL);
}

// Format timestamp for display
strftime(dateStr, sizeof(dateStr), "%Y-%m-%d", localtime(&records[i].date));
```

**What it teaches:**
- What a Unix timestamp is (`time_t` = seconds since Jan 1, 1970)
- How to calculate elapsed/remaining time using subtraction
- How `strftime` formats time like a date string
- How `localtime()` converts a `time_t` to a broken-down `struct tm`

---

### 6. 🔁 Loops and Control Flow

The main game loop, input loop, and all menus rely on standard loop patterns:

```c
// do-while for menu (runs at least once)
do {
    // show menu, get input
} while (choice != 6);

// for loop for scoreboard sorting and display
for (int i = 0; i < recordCount - 1; i++)
    for (int j = 0; j < recordCount - i - 1; j++)
        if (records[j].wpm < records[j+1].wpm) { /* swap */ }

// while loop for typing test (time-based exit)
while (time(NULL) < endTime) {
    if (_kbhit()) { /* read key */ }
    Sleep(40);
}
```

---

### 7. 📊 Sorting — Bubble Sort

The scoreboard is sorted by WPM using a classic **Bubble Sort** algorithm:

```c
for (int i = 0; i < recordCount - 1; i++) {
    for (int j = 0; j < recordCount - i - 1; j++) {
        if (records[j].wpm < records[j+1].wpm) {
            ScoreRecord tmp = records[j];
            records[j]      = records[j+1];
            records[j+1]    = tmp;
        }
    }
}
```

**What it teaches:**
- Swapping two struct values using a temporary variable
- How Bubble Sort works in O(n²) time
- Sorting in descending order (flip the comparison to `<`)

---

### 8. 🎲 Random Number Generation — `stdlib.h`

A random text passage is selected each time the test starts:

```c
srand((unsigned)time(NULL));       // seed with current time (different every run)
int selectedLine = rand() % lineCount;   // pick a random index
```

**What it teaches:**
- Why you must call `srand()` once before using `rand()`
- Using `time(NULL)` as a seed to get different results each run
- The modulo operator `%` to keep the result within a valid range

---

### 9. 🖨️ Formatted Output — `printf` with Format Specifiers

The entire UI — tables, boxes, headings — is built using carefully formatted `printf` statements:

```c
printf("| %-16s | %5d | %7d%% | %7.1f%% |\n",
        username, wpm, accuracy, consistency);
```

| Specifier | Meaning |
|---|---|
| `%-16s` | Left-align string in 16 chars |
| `%5d` | Right-align integer in 5 chars |
| `%7.1f` | Float with 7 total chars, 1 decimal |
| `%%` | Literal `%` character |

**What it teaches:**
- How field-width specifiers create aligned columns in plain text tables
- Left (`-`) vs right alignment
- Formatting floats with precision control

---

### 10. 🧩 Functions & Modular Design

The entire program is broken into focused single-purpose functions:

```c
void loadUsers();          // reads users.txt into array
void saveUsers();          // writes array back to users.txt
void typingTest(int dur);  // runs one test session
void showScoreboard();     // displays top 10
int  login();              // returns 1 on success, 0 on failure
```

**What it teaches:**
- How to break a large program into smaller, manageable pieces
- The difference between `void` functions and functions that return values
- Passing parameters (like `int duration`) to make functions reusable
- Function prototypes declared before `main()`

---

### 11. 🪟 Windows API — `windows.h`

Two Windows-specific functions are used:

```c
#include <windows.h>

Sleep(40);          // pause execution for 40 milliseconds
system("cls");      // clear the terminal screen
```

**What it teaches:**
- How to use platform-specific headers for OS features
- Why `Sleep()` (capital S) is Windows, while `usleep()` is Linux/Mac
- How `system()` runs a shell command from inside a C program

---

## 🎓 How This Game Was Built Using College-Level C Knowledge

If you have completed a standard **first or second year C programming course**, you already know enough to build DR.Typing. Here is the step-by-step thought process behind building it from scratch:

### Step 1 — Design the Data Model
> *"What information do I need to store?"*

Think of the two main entities: **Users** and **Scores**. Model each as a `struct`. This is exactly what you learn in your Data Structures unit.

### Step 2 — Persist Data with File I/O
> *"How do I save data between runs?"*

Use `fopen`/`fscanf`/`fprintf`/`fclose` — the File I/O chapter from your C textbook. Write a `loadX()` function that reads a `.txt` file into an array on startup, and a `saveX()` function that writes the array back on exit.

### Step 3 — Build the Login System
> *"How do I check a username and password?"*

Loop through your `users[]` array and use `strcmp()` to compare. If both match, set a global `currentUser` string. This uses arrays, loops, and string functions — all first-year topics.

### Step 4 — Implement the Real-Time Typing Loop
> *"How do I read keys without pausing the program?"*

Replace `scanf` with `_kbhit()` + `_getch()` from `conio.h`. Wrap it in a `while(time(NULL) < endTime)` loop. This is where `time.h` comes in — subtract timestamps to get a countdown.

### Step 5 — Calculate the Score
> *"How do I measure WPM and accuracy?"*

Loop through the typed string character by character, compare each with the target string, and count matches. Then apply the WPM formula (see below). This is just arrays, loops, and arithmetic.

### Step 6 — Display Results and Save the Record
> *"How do I show results neatly and remember them?"*

Use formatted `printf` with width specifiers to build aligned tables. Append the score to your `records[]` array and call `saveRecords()`.

### Step 7 — Rank Players on a Scoreboard
> *"How do I show the top 10 players?"*

Apply Bubble Sort on the `records[]` array sorted by `wpm`. Print the top 10. Pure arrays + sorting — your Data Structures 101.

---

## 🗂️ Data Structures Used

| Structure | Type | Purpose |
|---|---|---|
| `User users[100]` | Array of structs | In-memory database of all registered users |
| `ScoreRecord records[1000]` | Array of structs | In-memory database of all test results |
| `char input[]` | Character array (string) | Stores what the user types in real time |
| `char line[]` | Character array (string) | Stores the randomly selected target passage |
| `char *lines[]` | Array of pointers | Used for word-wrap line splitting |

---

## 💾 File Handling in Detail

DR.Typing uses **plain-text flat files** as its database — no SQL, no binary files.

### `users.txt` format
```
Debadatta mypassword123
Rohit     secret456
Priya     typing789
```
Each line: `username password` separated by a space.

### `records.txt` format
```
Debadatta 82 96 5 89 430 98.20 1718182050
Rohit     74 91 11 80 391 94.10 1718095650
```
Each line: `username wpm accuracy mistakes raw charsTyped consistency unixTimestamp`

### `text_15.txt` ... `text_150.txt` format
```
The quick brown fox jumps over the lazy dog.
Programming is the art of telling another human...
```
Each line is one complete passage. A random line number is selected using `rand() % lineCount`.

---

## 🎮 Game Logic Explained

```
Program Start
     │
     ├─► loadUsers()       ← read users.txt into users[]
     ├─► loadRecords()     ← read records.txt into records[]
     ├─► createTextFiles() ← create text_*.txt if not exist
     │
     ├─► displayWelcome()  ← show login/register screen
     ├─► login()           ← authenticate, set currentUser
     │
     └─► mainMenu() ──loop──┐
              │              │
              ├─ typingTest()─┤  ← select random text → timed input loop → score
              ├─ showScoreboard()  ← sort records[] by WPM → print top 10
              ├─ showPersonalRecords() ← filter records[] by currentUser
              ├─ showAbout()
              ├─ showContact()
              └─ Exit ──────┘
                    │
                    ├─► saveUsers()
                    └─► saveRecords()
```

---

## 📐 WPM & Accuracy Formula

The same formulas used by MonkeyType and TypeRacer:

### Words Per Minute (WPM)
```
WPM = (correctChars / 5) / (duration / 60.0)
```
> 1 "word" = 5 characters (industry standard). Divide correct chars by 5 to get words. Divide test duration in seconds by 60 to get minutes.

### Raw WPM (no mistake penalty)
```
Raw WPM = (totalCharsTyped / 5) / (duration / 60.0)
```

### Accuracy
```
Accuracy (%) = (correctChars / totalChars) * 100
```

### Consistency
```
Consistency (%) = (correctChars / totalCharsTyped) * 100
```
> How many of the characters you *actually typed* were correct — measures typing discipline.

### Example
```
Test duration  : 50 seconds
Correct chars  : 241
Total chars    : 268
Chars typed    : 249

WPM            = (241 / 5) / (50 / 60) = 48.2 / 0.833 = 57 WPM
Raw WPM        = (249 / 5) / 0.833     = 59.8          = 59 Raw
Accuracy       = (241 / 268) * 100     = 89.9%
Consistency    = (241 / 249) * 100     = 96.8%
```

---

## 🔧 Key Functions Reference

| Function | Return | Description |
|---|---|---|
| `loadUsers()` | `void` | Reads `users.txt` into `users[]` array |
| `saveUsers()` | `void` | Writes `users[]` array back to `users.txt` |
| `loadRecords()` | `void` | Reads `records.txt` into `records[]` array |
| `saveRecords()` | `void` | Writes `records[]` to `records.txt` |
| `createTextFiles()` | `void` | Creates passage files if they don't exist yet |
| `login()` | `int` | Returns `1` on successful login, `0` on failure |
| `registerUser()` | `void` | Adds a new user to `users[]` and saves |
| `mainMenu()` | `void` | Main do-while loop that drives the entire app |
| `typingTest(int dur)` | `void` | Runs a full timed test and calls `showResults` |
| `showResults(...)` | `void` | Displays the score table and saves the record |
| `showScoreboard()` | `void` | Sorts all records by WPM, prints top 10 |
| `showPersonalRecords()` | `void` | Filters and prints records for `currentUser` |
| `displayTextInBox(char*)` | `void` | Word-wraps text into a fixed-width terminal box |
| `printHeading(char*)` | `void` | Prints a decorated `.:*` section heading |
| `displayWelcome()` | `void` | Shows the splash screen |
| `clearScreen()` | `void` | Calls `system("cls")` to clear terminal |
| `myDelay(int ms)` | `void` | Calls `Sleep(ms)` to pause for milliseconds |

---

## Screenshots

<img width="1288" height="862" alt="image" src="https://github.com/user-attachments/assets/8fff1fa4-1ecd-4466-bd88-a9138d7698d3" />

<img width="851" height="748" alt="image" src="https://github.com/user-attachments/assets/a8262a75-b02f-4275-8318-6da787720c29" />

<img width="1281" height="703" alt="image" src="https://github.com/user-attachments/assets/4151f26c-cb89-41a8-b8df-3eb69467759c" />

<img width="944" height="904" alt="image" src="https://github.com/user-attachments/assets/d872d1d5-003a-49f9-8939-9ac3ebac7760" />

<img width="1367" height="794" alt="image" src="https://github.com/user-attachments/assets/48833a9b-47b2-4d65-b3f6-92bbf2926b9a" />

<img width="1330" height="700" alt="image" src="https://github.com/user-attachments/assets/55951c1a-984f-49b9-8dce-ba2aa0547b41" />









## ⚠️ Known Limitations

- **Windows only** — uses `<conio.h>`, `<windows.h>`, and `system("cls")`. Not portable to Linux/Mac without changes.
- **Plain-text storage** — passwords are stored in plain text. Not suitable for production use.
- **No backspace shown live** — the typed text display on one line doesn't visually update the cursor position mid-word on all terminals.
- **Single-file architecture** — all code is in one `.c` file. Larger projects would split into multiple `.h` and `.c` files.

---

## 🚀 Future Improvements

- [ ] Port to cross-platform using `ncurses` (Linux/Mac support)
- [ ] Hash passwords using a simple algorithm (e.g., XOR or MD5)
- [ ] Add colour using ANSI escape codes or Windows `SetConsoleTextAttribute`
- [ ] Add a multiplayer hotseat mode (two players alternate on the same machine)
- [ ] Add difficulty levels (punctuation-heavy, code snippets, numbers)
- [ ] Add a graph of personal WPM progress over time using ASCII bar charts
- [ ] Split code into multiple files (`auth.c`, `game.c`, `ui.c`, `records.c`)

---

## 👨‍💻 Author

**Debadatta Rout**

> *"This project was built as a way to learn C by doing — not just reading. Every concept in this README was discovered by hitting an error, Googling it, and figuring it out. If you're a student reading this: you can build this too."*

| Contact | Details |
|---|---|
| 📧 Email | routdebadatta22@gmail.com |
| 📞 Phone | +91 9827068499 |
| 💼 LinkedIn | [linkedin.com/in/debadatta-rout-454935341](http://www.linkedin.com/in/debadatta-rout-454935341) |

---

<div align="center">

**Built with ❤️ and lots of `printf` debugging**

*DR.Typing — Where every keystroke counts*

</div>
