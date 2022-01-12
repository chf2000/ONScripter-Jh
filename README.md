# ONScripter-Jh
This is a fork of [ONScripter-Jh] aimed at fixing bugs on modern platforms and adding more functionalities.  
This repo is forked from public archived https://github.com/fybmain/ONScripter-Jh.git by fybmain due to in inaccessibility of original repo on bitbucket.org.   

LISCENCE:[GPLv2][]

Onscripter是一个用来解析NScripter脚本的第三方开源Galgame游戏引擎，主要由Ogapee（<ogapee@aqua.dti2.ne.jp>）开发维护。

[ONScripter-Jh][]修改自[ONScripter][]，旨在在兼容原版[Onscripter][]的前提下，添加中文支持，提高性能，增加功能，发起人为h j（<https://bitbucket.org/jh10001/>）。

* Added a SW/HW renderer switch. ONScripter-Jh will use the software renderer of SDL2 by default due to terrible flickering under any hardware renderer including OpenGL, Vulkan and Metal on macOS. 
* No more bug fixes.

## Dependency
### Compiler:  
clang # on macOS and Linux  
cl # on windows  
### Make:  
GNU make # on macOS and Linux  
nmake # on windows  
### Library:  
SDL2  
lua  
sdl2-image  
sdl2-ttf  
sdl2-mixer  
bz2  
fontconfig  
smpeg2  
libjpeg  
libogg  
libvorbis-dev


## Compile

* macOS：
```bash
# install dependencies with homebrew and it will solve most of the problems
make -f Makefile.MacOSX
./onscripter -h
```

* GNU/Linux:
```bash
# install dependencies with your package manager and solve some problems involving path definitions manually 
#
# For Debian/Ubuntu users:
# lib*-dev libraries are essential when compiling on Debian/Ubuntu, which may contain different filenames other than their counterparts defined in header files of the project 
# manual modification is required under such circumstance
make -f Makefile.Linux
./onscripter -h
```

* Windows:
```powershell
# setup vcpkg then download and build all the dependencies with nesscessary flags
# modify Makefile.Win according to your environment
nmake -f Makefile.Win
# manually link the .obj files due to changes of M$ linker's parameter
# gather all Dynamic Link Libraries required so that onscripter can find them
./onscripter -h
```

## Test
* macOS  
OS Version: macOS 12.0.1 Darwin21.1.0  
Toolchain: Apple clang version 13.0.0 (clang-1300.0.29.3)  
Target: x86_64-apple-darwin21.1.0  
Thread model: posix  
SDK: MacOSX12.0.sdk  
Status: Pass  

* Linux  
OS Version: Ubuntu 20.04.3 LTS GNU/Linux 5.10.60.1-microsoft-standard-WSL2  
Toolchain: clang version 10.0.0-4ubuntu1  
Target: x86_64-pc-linux-gnu  
Thread model: posix  
Status: Pass    

* Linux  
OS Version: Debian 4.19.208-1 aarch64 GNU/Linux  
Toolchain: clang version 7.0.1-8+deb10u2 (tags/RELEASE_701/final)  
Target: aarch64-unknown-linux-gnu  
Thread model: posix  
Status: Pass  

* Windows  
OS Version: Windows 11 21H2 version 22000.318  
Toolchain: MSVC v143 - VS2022  
Target: x86 win32 & x64 win32  
SDK: Windows 10 SDK 10.0.19041.0  
Status: Pass  


## TODO  
* Test on Arm based Macs.

[GPLv2]: https://www.gnu.org/licenses/old-licenses/gpl-2.0.html
[ONScripter]: https://onscripter.osdn.jp/onscripter.html
[ONScripter-Jh]: https://bitbucket.org/jh10001/onscripter-jh

