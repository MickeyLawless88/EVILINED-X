# evilined-x --- Advanced Visual Line Editor

## Table of Contents

-   [Overview](#overview)
-   [Features](#features)
-   [Installation & Compilation](#installation--compilation)
-   [Basic Usage](#basic-usage)
-   [Command Reference](#command-reference)
-   [Visual Mode](#visual-mode)
-   [Customization Guide](#customization-guide)
-   [File Type Extensions](#file-type-extensions)
-   [Advanced Modifications](#advanced-modifications)
-   [Platform Support](#platform-support)
-   [License](#license)
-   [Contributing](#contributing)

## Overview

**evilined-x** (Enhanced Visual Line Editor --- eXtended) is a hybrid
line editor that combines the discipline of classic EDLIN with a fast
full-screen visual editor.

Designed specifically for **real DOS and vintage PC hardware**,
evilined-x runs on **8088/8086 and NEC V20/V30 systems**, making it
ideal for authentic retro environments.

Unlike most Vi clones, evilined-x does not require protected mode,
extended memory, or VGA graphics.

## Features

### Core Line Editor

-   Zero-padded line numbers
-   Case-insensitive commands
-   Multi-line insert mode
-   Range parsing (a,b)
-   Advanced search and replace
-   Interactive prompts with context
-   Robust bounds-checked memory handling

### Visual Mode

-   Full-screen editing
-   Arrow key navigation
-   Page Up / Page Down scrolling
-   Home / End navigation
-   Real-time status bar
-   Function key shortcuts

### Startup Banner

-   ASCII banner with version info
-   File status and line count
-   System clock
-   Platform compatibility display

## Installation & Compilation

### DOS Compilation

``` bat
tcc -ml EVILINED.C -o EVILINED.EXE
bcc -ml EVILINED.C -o EVILINED.EXE
cl /AL EVILINED.C /FeEVILINED.EXE
```

Large memory model is recommended.

## Basic Usage

``` bat
EVILINED
EVILINED myfile.txt
```

Workflow: 1. Start the editor 2. Edit in line mode 3. Enter visual mode
with `V` 4. Save with `W` or `F2` 5. Exit with `Q` or `ESC`

## Command Reference

  Command   Description
  --------- -------------
  L         List lines
  I         Insert
  D         Delete
  E         Edit
  R         Replace
  S         Search
  O         Open file
  W         Write file
  V         Visual mode
  Q         Quit

## Visual Mode

Status bar example:

    F1=Help F2=Save ESC=Exit | Line 15/234 Col 42 | myfile.c | C source file

## Customization Guide

evilined-x is intentionally hackable. File type detection, banner text,
commands, and colors are all easy to modify.

## File Type Extensions

Supports many classic languages including: - C / C++ - FORTRAN - BASIC -
Pascal - Assembly - COBOL

## Advanced Modifications

-   Optional line numbering
-   Auto-save
-   Undo stack
-   Statistics commands

All features are written to remain 8088-safe.

## Platform Support

-   CPU: 8088 / 8086 / NEC V20 / V30
-   RAM: 512 KB minimum
-   Display: CGA / EGA / VGA / Hercules
-   DOS: MS-DOS, PC-DOS, DR-DOS

## License

GNU General Public License v3.0

Copyright (C) 2025 Mickey Lawless

## Contributing

Preserve DOS compatibility, avoid protected mode assumptions, and test
on real hardware or accurate emulators.
