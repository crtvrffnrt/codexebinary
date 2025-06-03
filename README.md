
This repository contains a minimal WinAPI example that displays the
current time in a 300x100 window.  The program can be cross‑compiled on
Debian to produce a 32‑bit Windows executable.

## Building on Debian

1. Install the MinGW toolchain:

   ```bash
   sudo apt-get install g++-mingw-w64-i686
   ```

2. Compile the program:

   ```bash
   i686-w64-mingw32-g++ -static -Os clock.cpp -o clock.exe -lgdi32
   ```

   The resulting `clock.exe` can be run on Windows or tested on Linux
   using [Wine](https://www.winehq.org/):

   ```bash
   wine clock.exe
   ```