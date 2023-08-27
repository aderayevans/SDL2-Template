# SDL2-Template

Source:
* MSYS2: https://www.msys2.org/
* MinGW-W64: GCC-8.1.0 x86_64-win32-seh https://sourceforge.net/projects/mingw-w64/
* https://github.com/libsdl-org/SDL.git
* https://github.com/libsdl-org/SDL_image.git

## For Windows (x64):
Download Msys2 msys2-x86_64 https://github.com/msys2/msys2-installer/releases/download/2023-07-18/msys2-x86_64-20230718.exe

Install and run Msys2 `as administrator`
```shell
pacman -S mingw-w64-x86_64-toolchain cmake --noconfirm
```
Run the `build.bat` batch script to build the project

Run the `start.bat` to start the project

Could run those two batch scripts inside normal windows command line

## For Linux (Ubuntu specific):
sudo apt-get install -y \
    g++ libsdl2-2.0 libsdl2-dev \
    libsdl2-image-dev


Command to Build, Install and Run
```shell
cmake -S . -B bin/debug/ && sudo cmake --build bin/debug/ && bin/debug/SDL2_Template

or

./run
```
