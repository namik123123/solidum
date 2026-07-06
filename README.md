# Solidus (/) Programming Language

Solidus is a lightweight, C-style programming language designed to be simpler and faster to write than standard C.

## Installation

To install Solidus on your system, download this repository as a `.zip` file, extract it, and run the installer script for your Operating System:

### Linux / Ubuntu / Kubuntu
Open your terminal in the extracted folder and run:
```bash
chmod +x install.sh
./install.sh

Windows

Double-click install.bat or run it via Command Prompt (CMD).
macOS

Double-click install.command or run it via Terminal.
Usage

Once installed, restart your terminal and use the following commands:

    solidus run file./ - Run your Solidus code.

    solidus build file./ - Compile your Solidus code into a native binary.




## Language Documentation & Syntax

Solidus (`/`) is designed to be a cleaner, more intuitive version of C. Here is how you write code in Solidus:

### 1. Variables and Data Types
Unlike C, you don't need to worry about complex types like `int`, `float`, `double`, or `char*`. Solidus simplifies this into two main types:

| Solidus Syntax | Data Type | Internal C Representation |
| :--- | :--- | :--- |
| `var name = num 42` | Integers & Decimals | `double` (64-bit float) |
| `var name = str "me"` | Text Strings | `char*` (String literal) |

**Example:**
```text
var age = num 16.5
var username = str "namik123123"

2. The print() Function & String Interpolation

Printing data in Solidus is incredibly powerful. You don't need format specifiers like %d or %s. Just wrap your variable name in single quotes ' inside the string, and Solidus will handle the rest automatically!

Example:
Plaintext

var player = str "Steve"
var score = num 2500

print("Player 'player' has a score of 'score' points!")

3. Functions

Functions are defined using the short and clean fun keyword.

    No mandatory main function: You can write code freely at the root of the file (like a script), and the compiler will automatically wrap it into a hidden main block for C execution.

    You can still define your own custom functions anywhere in the file.

Example:
Plaintext

var greeting = str "Welcome to Solidus!"
print("'greeting'")

fun custom_log() {
    print("This is inside a custom function!")
}

// Call the function
custom_log()

4. Code Structure Example (file./)

Create a file named test./ and paste the following code:
Plaintext

var app_name = str "Solidus Compiler"
var version = num 1.0

print("Running 'app_name' version 'version'")

fun say_hello() {
    print("Hello from the function!")
}

say_hello()

Then run it using the command:
Bash

solidus run test./
