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

Command to Build, Install and Run
```shell
# only run this line the first time
cmake -G "MinGW Makefiles" -S . -B bin/debug/

# run these everytime after made changes and to execute the project
cmake --build bin/debug/ && start /b bin/debug/SDL2_Template.exe

# or Run the `windows_build.bat` batch script to build and start the project on windows
.\windows_build.bat
```

## For Linux (Ubuntu specific):
```shell
sudo apt-get install -y \
    g++ cmake libsdl2-2.0 libsdl2-dev \
    libsdl2-image-dev

git clone https://github.com/aderayevans/SDL2-Template.git

cd SDL2-Template

chmod +x ubuntu_build
```

Command to Build, Install and Run
```shell
# only run this line the first time
cmake -S . -B bin/debug/

# run these everytime after made changes and to execute the project
sudo cmake --build bin/debug/ && bin/debug/SDL2_Template

# or
./ubuntu_build
```
