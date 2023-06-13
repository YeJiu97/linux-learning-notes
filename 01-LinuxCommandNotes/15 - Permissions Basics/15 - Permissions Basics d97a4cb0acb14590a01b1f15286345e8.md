# 15 - Permissions Basics

Unix and unix-like systems are multiuser operating systems.

例子：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ cat /etc/sudoers
cat: /etc/sudoers: Permission denied
```

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled.png)

查看自己的id：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ id
uid=1000(yejiu97) gid=1000(yejiu97) groups=1000(yejiu97),4(adm),20(dialout),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),118(netdev)
```

我们可以看这样的一个例子：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ echo "hi" > greet.txt
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL$ ls -l greet.txt
-rwxrwxrwx 1 yejiu97 yejiu97 3 Dec 22 12:55 greet.txt
```

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled%201.png)

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled%202.png)

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled%203.png)

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled%204.png)

![Untitled](15%20-%20Permissions%20Basics%20d97a4cb0acb14590a01b1f15286345e8/Untitled%205.png)