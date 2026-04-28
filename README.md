# libft — Custom C Standard Library (42)

English | Español

---

## English

### Overview
**libft** is a foundational C project from **42 School** where you re-implement a selection of the standard C library functions, plus additional utilities (string/char handling, memory helpers, linked lists, etc.).

The goal is to build your own reusable library (`libft.a`) that you can link in future C projects.

### Features
- Re-implementation of common libc functions (`ft_strlen`, `ft_memcpy`, `ft_strncmp`, ...)
- Additional helpers (strings, chars, memory, conversions, etc.)
- Bonus: **linked list** utilities (`t_list` + `ft_lst*` functions) *(if included in your version)*
- Built as a static library: **libft.a**

### Requirements
- `cc` (clang or gcc)
- `make`

### Build
Compile the library:

```bash
make
```

### Clean
Remove object files:

```bash
make clean
```

Remove objects + library:

```bash
make fclean
```

Rebuild from scratch:

```bash
make re
```

### Usage
Include the header and link `libft.a` in your project.

Example:

```c
#include "libft.h"

int main(void)
{
    ft_putstr_fd("Hello from libft!\n", 1);
    return (0);
}
```

Compile with libft:

```bash
cc main.c -L. -lft -o app
```

> Depending on your Makefile, the library name might be `libft.a` and you may link it with `-lft` (common in 42) or directly specify the file: `cc main.c libft.a -o app`.

### Project structure (typical)
- `*.c` / `src/` — function implementations
- `libft.h` / `includes/` — public header(s)
- `Makefile` — build rules

---

## Español

### Descripción
**libft** es un proyecto base de **42 School** donde reimplementas una selección de funciones de la librería estándar de C, además de utilidades extra (manejo de strings/chars, helpers de memoria, listas enlazadas, etc.).

El objetivo es crear tu propia librería reutilizable (`libft.a`) para enlazarla en futuros proyectos en C.

### Características
- Reimplementación de funciones comunes de libc (`ft_strlen`, `ft_memcpy`, `ft_strncmp`, ...)
- Utilidades adicionales (strings, chars, memoria, conversiones, etc.)
- Bonus: utilidades de **listas enlazadas** (`t_list` + funciones `ft_lst*`) *(si están incluidas en tu versión)*
- Se compila como librería estática: **libft.a**

### Requisitos
- `cc` (clang o gcc)
- `make`

### Compilar
Compila la librería:

```bash
make
```

### Limpiar
Borrar archivos objeto:

```bash
make clean
```

Borrar objetos + librería:

```bash
make fclean
```

Recompilar desde cero:

```bash
make re
```

### Uso
Incluye el header y enlaza `libft.a` en tu proyecto.

Ejemplo:

```c
#include "libft.h"

int main(void)
{
    ft_putstr_fd("Hola desde libft!\n", 1);
    return (0);
}
```

Compilar con libft:

```bash
cc main.c -L. -lft -o app
```

> Dependiendo de tu Makefile, el nombre de la librería puede ser `libft.a` y puedes enlazar con `-lft` (típico en 42) o directamente pasando el archivo: `cc main.c libft.a -o app`.
