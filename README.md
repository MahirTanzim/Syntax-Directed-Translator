# Syntax-Directed Translator for Simple Mathematical Expressions

## Project Description

The **Syntax-Directed Translator for Simple Mathematical Expressions** is a tool that translates simple arithmetic expressions into a target representation, such as assembly-like instructions (3-address code). The translator takes expressions like `2 + 3 * 4` and processes them based on operator precedence and associativity.
## What is Syntax Directed Translation(SDT)?
Syntax-directed translation (SDT) is a compiler implementation method where source language translation is driven by the parser, associating semantic actions and attributes with grammar rules to facilitate the transformation of source code into intermediate or target code. 





## Run Locally
### Prerequisites:
Ensure that you have **Bison** and **Flex** installed on your system. If not, follow the steps below for installation (specific to Ubuntu. If U are using Windows, you can suck you D).
#### Installing Bison and Flex (if not installed):
```bash
sudo apt update && sudo apt upgrade -y
sudo apt-get install bison flex
```

#### Clone the project:

```bash
  git clone https://link-to-project
```

#### Go to the project directory:

```bash
  cd my-project
```

#### Run Flex file:

```bash
  flex lexer.l
```
This will create a .c file named `lex.yy.c`.
#### Run Bison File:

```bash
  bison -d -t parser.y
```
This Will create two file named `parser.tab.c` and `parser.tab.h`.

#### Compile `lex.yy.c` and `parser.tab.c`:
```bash
  gcc lex.yy.c parser.tab.c -o sdt.out
```
After that an executable file named sdt.ou will be created. Which is our project.

#### Executing the program:
```bash
  ./sdt.out
```
Now the in the terminal the program will be asked for an  Mathematical expression to translate it into the 3 address code. 
