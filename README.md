# ft_printf

A project from the 42 curriculum. The goal of this project is to recode the `printf` function from the standard C library (`libc`).

By doing this, you learn how to handle a variable number of arguments (variadic functions) in C and deepen your understanding of formatting and outputting data.

## Supported Conversions

This implementation of `ft_printf` supports the following basic format tags (found in files such as `case_c_s_d_i_u.c`):

* `%c` - Prints a single character.
* `%s` - Prints a string of characters.
* `%d` - Prints a signed decimal (base 10) number.
* `%i` - Prints an integer (base 10).
* `%u` - Prints an unsigned decimal (base 10) number.

*(Feel free to add `%p`, `%x`, `%X`, and `%%` here if your complete project supports them as well)*

## Compilation and Usage

### 1. Build the library

Clone the repository and run the `make` command to compile the static library `libftprintf.a`:

```bash
git clone <your-repo-url>
cd ft_printf
make
```

### 2. Use in your project

Include the header in your C files:

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s! I have %d apples.\n", "World", 42);
    return (0);
}
```

Compile your program together with the created library:

```bash
gcc -Wall -Wextra -Werror main.c libftprintf.a -o my_program
./my_program
```

## Structure (Example)

* `ft_printf.c` - The main function and the parsing of the format strings.
* `case_c_s_d_i_u.c` - Helper functions for printing characters, strings, and numbers (incl. `ft_putchar_pf`, `ft_putstr_pf`, `ft_putnbr_pf`, etc.).
* `ft_printf.h` - The header file containing all prototypes.

## Author

* **jschmunk** - *42 Student*