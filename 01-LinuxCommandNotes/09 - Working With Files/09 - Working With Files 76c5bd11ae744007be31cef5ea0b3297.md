# 09 - Working With Files

less file会将file中的内容显示出来，一次显示一页的内容。

对于特别大的文本，使用less会比只用cat来的更加的有用。

例子：

![Untitled](09%20-%20Working%20With%20Files%2076c5bd11ae744007be31cef5ea0b3297/Untitled.png)

按f之后，进入到下一页：

![Untitled](09%20-%20Working%20With%20Files%2076c5bd11ae744007be31cef5ea0b3297/Untitled%201.png)

按b可以回到上一页：

![Untitled](09%20-%20Working%20With%20Files%2076c5bd11ae744007be31cef5ea0b3297/Untitled%202.png)

每按一次可以往下移动一行：

![Untitled](09%20-%20Working%20With%20Files%2076c5bd11ae744007be31cef5ea0b3297/Untitled%203.png)

如果我们为 cat 提供多个文件，它将连接它们的内容并输出它们。

cat和tac的显示恰好相反：

![Untitled](09%20-%20Working%20With%20Files%2076c5bd11ae744007be31cef5ea0b3297/Untitled%204.png)

rev则是将内容左右调转：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
04  1.txt  2.txt  2_cp.txt  rev.txt  text.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat rev.txt
12345679
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ rev rev.txt
97654321
```

head和tail:

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
04  1.txt  2.txt  2_cp.txt  rev.txt  text.txt  word.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat word.txt
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ head word.txt
1
2
3
4
5
6
7
8
9
10
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ head -11 word.txt
1
2
3
4
5
6
7
8
9
10
11
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ tail word.txt
11
12
13
14
15
16
17
18
19
20
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ tail -11 word.txt
10
11
12
13
14
15
16
17
18
19
20
```

wc是wordcount的缩写：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls
04  1.txt  2.txt  2_cp.txt  rev.txt  text.txt  word.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ wc word.txt
19 20 69 word.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ wc rev.txt
 1  1 10 rev.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ wc text.txt
 40  39 217 text.txt
```