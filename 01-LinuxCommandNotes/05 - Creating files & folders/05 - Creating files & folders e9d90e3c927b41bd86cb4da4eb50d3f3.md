# 05 - Creating files & folders

## touch 和 mkdir

touch指令用来创建文件，而midir用来创建文件夹：

```bash
yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$ ls
03/  hello.txt

yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$ touch sayHi.txt

yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$ ls
03/  hello.txt  sayHi.txt

yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$ mkdir 04

yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$ ls
03/  04/  hello.txt  sayHi.txt

yinia@DESKTOP-S9ODFEQ MINGW64 ~/Desktop/WSL
$
```

## file指令

file指令如下所示：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
03  04  hello.txt  sayHi.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ file hello.txt
hello.txt: empty
```