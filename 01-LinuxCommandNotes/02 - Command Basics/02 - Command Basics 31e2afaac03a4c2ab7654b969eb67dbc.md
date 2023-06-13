# 02 - Command Basics

## Open Terminal

任何一个系统都应该提供了类似的一个终端：

![Untitled](02%20-%20Command%20Basics%2031e2afaac03a4c2ab7654b969eb67dbc/Untitled.png)

可以按Ctrl+ALT+T来打开。

## Some Commands

首先使用的是date指令，这个指令会返回系统的时间：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ date
Mon Dec 19 17:46:48 ACDT 2022
```

接着我们可以使用clear来清楚已经打印了的东西：

![Untitled](02%20-%20Command%20Basics%2031e2afaac03a4c2ab7654b969eb67dbc/Untitled%201.png)

![Untitled](02%20-%20Command%20Basics%2031e2afaac03a4c2ab7654b969eb67dbc/Untitled%202.png)

需要注意的地方在于date和Date是不同的：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ date
Mon Dec 19 17:48:44 ACDT 2022
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ Date
Command 'Date' not found, did you mean:
  command 'date' from deb coreutils (8.32-4.1ubuntu1)
  command 'late' from deb late (0.1.0-14)
  command 'kate' from deb kate (4:21.12.3-0ubuntu1)
Try: sudo apt install <deb name>
```

可以发现没有Date这个指令，linux会推荐一些相关联的指令。

另一个简单的指令是ncal：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ncal
    December 2022
Su     4 11 18 25
Mo     5 12 19 26
Tu     6 13 20 27
We     7 14 21 28
Th  1  8 15 22 29
Fr  2  9 16 23 30
Sa  3 10 17 24 31
```

## Command Structure

指令的结构如下所示：

![Untitled](02%20-%20Command%20Basics%2031e2afaac03a4c2ab7654b969eb67dbc/Untitled%203.png)

以echo为例子：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "Hello World"
Hello World
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo hello world
hello world
```

尝试一下ncal：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ncal 2021
                                  2021
    January           February          March             April
Su     3 10 17 24 31     7 14 21 28        7 14 21 28        4 11 18 25
Mo     4 11 18 25     1  8 15 22        1  8 15 22 29        5 12 19 26
Tu     5 12 19 26     2  9 16 23        2  9 16 23 30        6 13 20 27
We     6 13 20 27     3 10 17 24        3 10 17 24 31        7 14 21 28
Th     7 14 21 28     4 11 18 25        4 11 18 25        1  8 15 22 29
Fr  1  8 15 22 29     5 12 19 26        5 12 19 26        2  9 16 23 30
Sa  2  9 16 23 30     6 13 20 27        6 13 20 27        3 10 17 24

    May               June              July              August
Su     2  9 16 23 30     6 13 20 27        4 11 18 25     1  8 15 22 29
Mo     3 10 17 24 31     7 14 21 28        5 12 19 26     2  9 16 23 30
Tu     4 11 18 25     1  8 15 22 29        6 13 20 27     3 10 17 24 31
We     5 12 19 26     2  9 16 23 30        7 14 21 28     4 11 18 25
Th     6 13 20 27     3 10 17 24        1  8 15 22 29     5 12 19 26
Fr     7 14 21 28     4 11 18 25        2  9 16 23 30     6 13 20 27
Sa  1  8 15 22 29     5 12 19 26        3 10 17 24 31     7 14 21 28

    September         October           November          December
Su     5 12 19 26        3 10 17 24 31     7 14 21 28        5 12 19 26
Mo     6 13 20 27        4 11 18 25     1  8 15 22 29        6 13 20 27
Tu     7 14 21 28        5 12 19 26     2  9 16 23 30        7 14 21 28
We  1  8 15 22 29        6 13 20 27     3 10 17 24        1  8 15 22 29
Th  2  9 16 23 30        7 14 21 28     4 11 18 25        2  9 16 23 30
Fr  3 10 17 24        1  8 15 22 29     5 12 19 26        3 10 17 24 31
Sa  4 11 18 25        2  9 16 23 30     6 13 20 27        4 11 18 25
```

或者我们增加一个参数：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ncal 2024
                                  2024
    January           February          March             April
Su     7 14 21 28        4 11 18 25        3 10 17 24 31     7 14 21 28
Mo  1  8 15 22 29        5 12 19 26        4 11 18 25     1  8 15 22 29
Tu  2  9 16 23 30        6 13 20 27        5 12 19 26     2  9 16 23 30
We  3 10 17 24 31        7 14 21 28        6 13 20 27     3 10 17 24
Th  4 11 18 25        1  8 15 22 29        7 14 21 28     4 11 18 25
Fr  5 12 19 26        2  9 16 23        1  8 15 22 29     5 12 19 26
Sa  6 13 20 27        3 10 17 24        2  9 16 23 30     6 13 20 27

    May               June              July              August
Su     5 12 19 26        2  9 16 23 30     7 14 21 28        4 11 18 25
Mo     6 13 20 27        3 10 17 24     1  8 15 22 29        5 12 19 26
Tu     7 14 21 28        4 11 18 25     2  9 16 23 30        6 13 20 27
We  1  8 15 22 29        5 12 19 26     3 10 17 24 31        7 14 21 28
Th  2  9 16 23 30        6 13 20 27     4 11 18 25        1  8 15 22 29
Fr  3 10 17 24 31        7 14 21 28     5 12 19 26        2  9 16 23 30
Sa  4 11 18 25        1  8 15 22 29     6 13 20 27        3 10 17 24 31

    September         October           November          December
Su  1  8 15 22 29        6 13 20 27        3 10 17 24     1  8 15 22 29
Mo  2  9 16 23 30        7 14 21 28        4 11 18 25     2  9 16 23 30
Tu  3 10 17 24        1  8 15 22 29        5 12 19 26     3 10 17 24 31
We  4 11 18 25        2  9 16 23 30        6 13 20 27     4 11 18 25
Th  5 12 19 26        3 10 17 24 31        7 14 21 28     5 12 19 26
Fr  6 13 20 27        4 11 18 25        1  8 15 22 29     6 13 20 27
Sa  7 14 21 28        5 12 19 26        2  9 16 23 30     7 14 21 28

yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ncal April 2024
    April 2024
Su     7 14 21 28
Mo  1  8 15 22 29
Tu  2  9 16 23 30
We  3 10 17 24
Th  4 11 18 25
Fr  5 12 19 26
Sa  6 13 20 27
```

可以发现我们可以指定某一年的某一个月。

有一个名为colours的txt文件：

![Untitled](02%20-%20Command%20Basics%2031e2afaac03a4c2ab7654b969eb67dbc/Untitled%204.png)

接着我们来使用sort指令，并且给出这个文件名作为参数：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ ls
colours.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ sort colours.txt
blue
green
indigo
orange
red
violet
yellow
```

接着我们来使用rm来移除文件：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ ls
colours.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ rm colours.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ ls
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$
```