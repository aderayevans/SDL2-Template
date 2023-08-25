# SDL2-Template

Source:
* SDL2: SDL2-devel-2.26.1-mingw.zip https://github.com/libsdl-org/SDL
* SDL2 Image: SDL2_image-devel-2.6.2-mingw.zip https://github.com/libsdl-org/SDL_image
* MinGW-W64: GCC-8.1.0 x86_64-win32-seh https://sourceforge.net/projects/mingw-w64/

For Linux (Ubuntu specific):
sudo apt-get install -y \
    g++ libsdl2-2.0 libsdl2-dev \
    libsdl2-image-dev

Command to Build, Install and Run
```shell
cmake -S . -B bin/debug/ && sudo cmake --build bin/debug/ && bin/debug/SDL2_Template

or

./run
```
