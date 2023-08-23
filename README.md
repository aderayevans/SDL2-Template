# SDL2-Template

Source:
* SDL2: SDL2-devel-2.26.1-mingw.zip https://github.com/libsdl-org/SDL
* SDL2 Image: SDL2_image-devel-2.6.2-mingw.zip https://github.com/libsdl-org/SDL_image
* MinGW-W64: GCC-8.1.0 x86_64-win32-seh https://sourceforge.net/projects/mingw-w64/

For Linux (Ubuntu specific):
sudo apt-get install -y \
    g++ libsdl2-2.0 libsdl2-dev 
    libsdl2-image-dev libsdl-image1.2-dev
    libsdl2-ttf-dev libsdl-ttf2.0-dev

pacman -S mingw-w64-x86_64-toolchain cmake mingw-w64-x86_64-SDL2 mingw-w64-x86_64-SDL2_image mingw-w64-x86_64-SDL2_ttf --noconfirm

Command to Build, Install and Run
```shell
cmake -S . -B bin/debug/

sudo cmake --build bin/debug/ --target install
```

Path: 
* D:/Programs/SDL2-w64  (extract both SDL2 & SDL2 Image to this path)
* D:/Programs/mingw64
