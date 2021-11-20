# ONScripter-Jh
This is a fork of [ONScripter-Jh] aimed at fixing bugs on modern platforms and adding more functionalities.
This repo is forked from public archived https://github.com/fybmain/ONScripter-Jh.git by fybmain due to in inaccessibility of original repo on bitbucket.org.

LISCENCE:[GPLv2][]

Onscripter是一个用来解析NScripter脚本的第三方开源Galgame游戏引擎，主要由Ogapee（<ogapee@aqua.dti2.ne.jp>）开发维护。

[ONScripter-Jh][]修改自[ONScripter][]，旨在在兼容原版[Onscripter][]的前提下，添加中文支持，提高性能，增加功能，发起人为h j（<https://bitbucket.org/jh10001/>）。

## Compile

* macOS：
```
$ make -f Makefile.MacOSX
$ ./onscripter
```

## Test
* macOS
OS Version: macOS 12.0.1
Toolchain: Apple clang version 13.0.0 (clang-1300.0.29.3)
Target: x86_64-apple-darwin21.1.0
Thread model: posix
SDK: MacOSX12.0.sdk
Status: Pass

* Linux
Status: Pending

## TODO
* Test on more platforms.
* Add more functionalities.

[GPLv2]: https://www.gnu.org/licenses/old-licenses/gpl-2.0.html
[ONScripter]: https://onscripter.osdn.jp/onscripter.html
[ONScripter-Jh]: https://bitbucket.org/jh10001/onscripter-jh

