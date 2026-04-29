# 42 Rush02 ASCII Rectangle

A C project developed during the 42 Piscine that prints a rectangle in ASCII using different characters for corners, borders, and inner spaces. 

## About the project

This project is based on a classic 42 rush exercise: generating a rectangle from two dimensions, width and height, and printing it directly to the terminal. The program is organized into small functions so that each part of the logic has a clear responsibility.

The current project is divided into three source files:  
- `main.c`: starts the program and calls the main `rush` function. 
- `ft_putchar.c`: prints one character at a time using `write`. 
- `rush02.c`: contains the rectangle logic, input validation, and the functions responsible for the first, middle, and last lines.

The rectangle is built with:
- `A` for the top corners,
- `C` for the bottom corners,
- `B` for borders, 
- spaces for the inside of the rectangle.

For the test used in `main.c`, the program calls `rush(5, 3)`, so the output is based on a rectangle with width 5 and height 3. 

## How it works

The execution starts in `main`, which calls `rush(5, 3)`.  
Then the `rush` function checks whether the values are valid before starting the drawing process.

If the values are valid, the program uses nested loops:
- one loop for the lines, 
- one loop for the columns. 

Depending on the current position, the program decides which helper function to use:
- `ft_first()` for the first line, 
- `ft_middle()` for the middle lines,
- `ft_last()` for the last line.

Each helper function sends the correct character to `ft_putchar()`, which prints it to the terminal. 

## How to run

This project was made to run on Linux.

### 1. Compile

Use `gcc` to compile all source files:

```bash
gcc -Wall -Wextra -Werror main.c ft_putchar.c rush02.c -o rush02
```

### 2. Run

After compiling, run:

```bash
./rush02
```

## Expected output

With the current `main.c`, the program calls `rush(5, 3)`, so it should print a 5x3 rectangle. 

Example output:

```text
ABBBA
B   B
CBBBC
```
## Project result

This project received a score of **104**. 

## Notes

This project was built as a small modular C exercise focused on:
- function decomposition, 
- loops and conditionals, 
- terminal output with `write`, 
- and simple project organization.
