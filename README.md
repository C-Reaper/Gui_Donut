# Project README

## Overview
The project is a simple 3D donut visualization application. It uses a custom C library for rendering and handles user input through keyboard controls.

## Features
- Rendering of a 3D donut shape.
- User interaction via keyboard to rotate the donut (A, D, S, W keys).

## Project Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- GCC (GNU Compiler Collection) for building on Linux and Windows.
- MinGW-w64 for cross-compiling to Windows on Linux.
- Emscripten for compiling to WebAssembly.
- Standard development tools like make, gdb.

## Build & Run

### Linux
1. Navigate to the project directory:
   ```bash
   cd <Project>
   ```
2. Build the project:
   ```bash
   make -f Makefile.linux all
   ```
3. Execute the application:
   ```bash
   make -f Makefile.linux exe
   ```

### Windows (using MinGW-w64)
1. Navigate to the project directory:
   ```bash
   cd <Project>
   ```
2. Build the project:
   ```bash
   make -f Makefile.windows all
   ```
3. Execute the application:
   ```bash
   make -f Makefile.windows exe
   ```

### Wine (Cross-compiling to Windows on Linux)
1. Navigate to the project directory:
   ```bash
   cd <Project>
   ```
2. Build the project:
   ```bash
   make -f Makefile.wine all
   ```
3. Run the application in Wine:
   ```bash
   make -f Makefile.wine exe
   ```

### WebAssembly (using Emscripten)
1. Navigate to the project directory:
   ```bash
   cd <Project>
   ```
2. Build the project:
   ```bash
   make -f Makefile.web all
   ```
3. Run the application in a web browser:
   ```bash
   make -f Makefile.web exe
   ```

### Clean Rebuild
To clean and rebuild the project, you can use:
```bash
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

Replace `(os)` with `linux`, `windows`, `wine`, or `web` depending on your target platform.