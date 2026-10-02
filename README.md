*This project has been created as part of the 42 curriculum by xirwang.*

# Libft

## Description

`libft` is a custom C library reimplementing a selection of standard C library
(`libc`) functions, along with a set of additional utility functions and a
singly linked list implementation, all built from scratch. The goal of this
project is to build a personal toolkit of well-understood, thoroughly tested
functions that can be reused across future C projects in the 42 curriculum.

The library is split into three parts:
- **Part 1**: Reimplementations of standard `libc` functions (e.g. `strlen`,
  `memcpy`, `strchr`, `atoi`, ...) prefixed with `ft_`.
- **Part 2**: Additional string, array, and formatted-output utility functions
  not found in the standard `libc` (e.g. `ft_split`, `ft_itoa`, `ft_strjoin`).
- **Part 3**: A singly linked list (`t_list`) and a full set of
  functions to create, traverse, transform, and free linked lists.

## Instructions

### Compilation

Clone the repository and run `make` at the project root:

```bash
make        # builds libft.a (includes Part 1, Part 2, and Part 3)
make clean  # removes object files
make fclean # removes object files and libft.a
make re     # fclean + rebuild
```

This produces `libft.a`, a static library, at the root of the repository.

### Usage in another project

Copy the `libft.a` file and `libft.h` header (or the whole `libft/` folder)
into your project, then:

```c
#include "libft.h"
```

and compile/link with:

```bash
cc your_file.c -L path/to/libft -lft -o your_program
```

## Resources

- [The GNU C Library manual](https://www.gnu.org/software/libc/manual/)
- `man` pages for each reimplemented function (e.g. `man strlen`, `man memcpy`,
  `man strlcpy`)
- *The C Programming Language* — Kernighan & Ritchie
- [42 Norm documentation (intranet)]

### AI usage disclosure

Claude (Anthropic) was used as a learning aid during this project, strictly as
a discussion and reasoning partner rather than a code generator, in line with
42's AI guidelines:
- Explaining C concepts (pointers, `const`, `restrict`, static libraries,
  Makefile dependency/relink behavior, header guards).
- Discussing edge cases to consider before implementing a function (without
  being given the implementation itself).
- Reviewing reasoning and debugging strategy (e.g. how to use `valgrind`,
  how to structure test comparisons against the real `libc` functions).

No function implementation was written by AI; all `ft_*` functions were
written and debugged by the author.

## Library description

<!-- TODO: once the project is complete, describe each function you
implemented here — what it does, any notable implementation choices, and
edge cases you specifically handled. Example format below. -->

### Part 1 — Libc functions
- `ft_strlen` — ...
- `ft_memcpy` — ...
- (continue for every function)

### Part 2 — Additional functions
- `ft_substr` — ...
- `ft_split` — ...
- (continue for every function)

### Part 3 — Linked list
- `ft_lstnew` — ...
- `ft_lstmap` — ...
- (continue for every function)

## Testing

Each function was tested against its standard `libc` counterpart (where
applicable) with dedicated small test programs, and checked for memory leaks
using `valgrind --leak-check=full`.
