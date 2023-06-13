# 10 - Redirection

standard input在command的作用之下会有两个可能的结果：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled.png)

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%201.png)

redirection的逻辑为：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%202.png)

重定向输出符号 (>) 告诉 shell 将命令的输出重定向到特定文件而不是屏幕。

以date为例子：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
redirection.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ date
Mon Dec 19 22:56:50 ACDT 2022
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ date > date.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat date.txt
Mon Dec 19 22:56:58 ACDT 2022
```

更多的例子：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%203.png)

如果向同一个对象中redirection呢？

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "Hello" > test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt  test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat test.txt
Hello
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "World" > test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt  test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat test.txt
World
```

得到的结果如上所示。

如果想要添加而不是覆盖：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "Hello" > test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt  test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat test.txt
Hello
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "World" >> test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
date.txt  redirection.txt  test.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat test.txt
Hello
World
```

可以发现>会导致覆盖，而>>则是导致append。

如果是redirection input，则如下图所示：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%204.png)

组合如下图所示：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%205.png)

重定向standard error：

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%206.png)

![Untitled](10%20-%20Redirection%2044ed3ccfaba2494ea54c75d1499e17c8/Untitled%207.png)