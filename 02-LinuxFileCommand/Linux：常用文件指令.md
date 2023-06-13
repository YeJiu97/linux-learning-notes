# 01-常见文件管理命令

查看作业使用home：

```bash
acs@6c70dd798fbe:~$ homework
Usage: homework lesson_id [Option]
Option:
    show: 显示作业要求
    create: 创建作业环境
    test: 测试作业正确性
Example: homework 1 show：显示lesson_1的作业要求
acs@6c70dd798fbe:~$ homework 1 show
网页格式地址：https://www.acwing.com/file_system/file/content/whole/index/content/2855530/

1. 常用命令介绍
    (1) ctrl c: 取消命令，并且换行
    (2) ctrl u: 清空本行命令
    (3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
    (4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
    (5) pwd: 显示当前路径
    (6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
    (7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
    (8) mkdir XXX: 创建目录XXX
    (9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
    (10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
    (11) touch XXX: 创建一个文件
    (12) cat XXX: 展示文件XXX中的内容
    (13) 复制文本
        windows/Linux下：Ctrl + insert，Mac下：command + c
    (14) 粘贴文本
        windows/Linux下：Shift + insert，Mac下：command + v

2. 创建作业 & 测试作业的正确性
    homework 1 create 可以重新创建所有lesson_1的作业
    homework 1 create id 可以单独创建lesson_1的第id个作业. e.g.
        homework 1 create 0 可以只重新创建lesson_1的第0个作业
    homework 1 test 可以评测lesson_1的所有作业

3. 作业
    创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
    (0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c
    (1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak
    (2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt
    (3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下
    (4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除
    (5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除
    (6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作
    (7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
        将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
        将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
        将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;
    (8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作
    (9) 进入homework_9文件夹，将其中所有txt类型的文件删除
acs@6c70dd798fbe:~$
```

先进行一下test：

```bash
acs@6c70dd798fbe:~$ homework 1 test
homework_0 is Wrong.
homework_1 is Wrong.
homework_2 is Wrong.
homework_3 is Wrong.
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 0/100
```

可以发现所有的题目都是错误的，我们现在需要去完成这些作业。

操作如下所示：

```bash
acs@6c70dd798fbe:~/homework$ cd lesson_1
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ homework 1 show
网页格式地址：https://www.acwing.com/file_system/file/content/whole/index/content/2855530/

1. 常用命令介绍
    (1) ctrl c: 取消命令，并且换行
    (2) ctrl u: 清空本行命令
    (3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
    (4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
    (5) pwd: 显示当前路径
    (6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
    (7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
    (8) mkdir XXX: 创建目录XXX
    (9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
    (10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
    (11) touch XXX: 创建一个文件
    (12) cat XXX: 展示文件XXX中的内容
    (13) 复制文本
        windows/Linux下：Ctrl + insert，Mac下：command + c
    (14) 粘贴文本
        windows/Linux下：Shift + insert，Mac下：command + v

2. 创建作业 & 测试作业的正确性
    homework 1 create 可以重新创建所有lesson_1的作业
    homework 1 create id 可以单独创建lesson_1的第id个作业. e.g.
        homework 1 create 0 可以只重新创建lesson_1的第0个作业
    homework 1 test 可以评测lesson_1的所有作业

3. 作业
    创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
    (0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c
    (1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak
    (2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt
    (3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下
    (4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除
    (5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除
    (6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作
    (7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
        将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
        将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
        将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;
    (8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作
    (9) 进入homework_9文件夹，将其中所有txt类型的文件删除
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_0
acs@6c70dd798fbe:~/homework/lesson_1/homework_0$ ls
acs@6c70dd798fbe:~/homework/lesson_1/homework_0$ mkdir dir_a dir_b dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_0$ ls
dir_a  dir_b  dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_0$ homework 1 test
homework_0 is Right!
homework_1 is Wrong.
homework_2 is Wrong.
homework_3 is Wrong.
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 10/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_0$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_1
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ ls
a.txt  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ cp a.txt a.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ ls
a.txt  a.txt.bak  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ c.txt c.txt.bak
-bash: c.txt: command not found
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ cp b.txt b.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ ls
a.txt  a.txt.bak  b.txt  b.txt.bak  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ cp c.txt c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ ls
a.txt  a.txt.bak  b.txt  b.txt.bak  c.txt  c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ hoemwork 1 test 1
-bash: hoemwork: command not found
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ hoemwork 1 test  
-bash: hoemwork: command not found
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Wrong.
homework_3 is Wrong.
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 20/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_1$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ homework 1 show
网页格式地址：https://www.acwing.com/file_system/file/content/whole/index/content/2855530/

1. 常用命令介绍
    (1) ctrl c: 取消命令，并且换行
    (2) ctrl u: 清空本行命令
    (3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
    (4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
    (5) pwd: 显示当前路径
    (6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
    (7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
    (8) mkdir XXX: 创建目录XXX
    (9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
    (10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
    (11) touch XXX: 创建一个文件
    (12) cat XXX: 展示文件XXX中的内容
    (13) 复制文本
        windows/Linux下：Ctrl + insert，Mac下：command + c
    (14) 粘贴文本
        windows/Linux下：Shift + insert，Mac下：command + v

2. 创建作业 & 测试作业的正确性
    homework 1 create 可以重新创建所有lesson_1的作业
    homework 1 create id 可以单独创建lesson_1的第id个作业. e.g.
        homework 1 create 0 可以只重新创建lesson_1的第0个作业
    homework 1 test 可以评测lesson_1的所有作业

3. 作业
    创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
    (0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c
    (1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak
    (2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt
    (3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下
    (4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除
    (5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除
    (6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作
    (7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
        将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
        将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
        将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;
    (8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作
    (9) 进入homework_9文件夹，将其中所有txt类型的文件删除
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv a.txt a.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv b.txt b.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv c.txt c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ ls
a.txt.bak  b.txt.bak  c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Wrong.
homework_3 is Wrong.
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 20/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv a.txt.bak a_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv b.txt.bak b_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ mv c.txt.bak c_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ ls
a_new.txt  b_new.txt  c_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Wrong.
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 30/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_2$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_3
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ ls
dir_a  dir_b
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ mv ./dir_a/a.txt ./dir_b
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ ls ./dir_a
b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ mv ./dir_a/b.txt ./dir_b
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ mv ./dir_a/c.txt ./dir_b
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ ls ./dir_b
a.txt  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 40/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_3$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_4
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ ls
a.txt  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Wrong.
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 40/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ homework 1 show
网页格式地址：https://www.acwing.com/file_system/file/content/whole/index/content/2855530/

1. 常用命令介绍
    (1) ctrl c: 取消命令，并且换行
    (2) ctrl u: 清空本行命令
    (3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
    (4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
    (5) pwd: 显示当前路径
    (6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
    (7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
    (8) mkdir XXX: 创建目录XXX
    (9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
    (10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
    (11) touch XXX: 创建一个文件
    (12) cat XXX: 展示文件XXX中的内容
    (13) 复制文本
        windows/Linux下：Ctrl + insert，Mac下：command + c
    (14) 粘贴文本
        windows/Linux下：Shift + insert，Mac下：command + v

2. 创建作业 & 测试作业的正确性
    homework 1 create 可以重新创建所有lesson_1的作业
    homework 1 create id 可以单独创建lesson_1的第id个作业. e.g.
        homework 1 create 0 可以只重新创建lesson_1的第0个作业
    homework 1 test 可以评测lesson_1的所有作业

3. 作业
    创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
    (0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c
    (1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak
    (2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt
    (3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下
    (4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除
    (5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除
    (6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作
    (7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
        将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
        将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
        将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;
    (8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作
    (9) 进入homework_9文件夹，将其中所有txt类型的文件删除
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ rm a.txt b.txt c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ ls
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Wrong.
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 50/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_4$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_5
acs@6c70dd798fbe:~/homework/lesson_1/homework_5$ ls
dir_a  dir_b  dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_5$ rm -rf dir_a dir_b dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_5$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Right!
homework_6 is Wrong.
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 60/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_5$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ homework_6
-bash: homework_6: command not found
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_6
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ ls
task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ cat task.txt
将task.txt重命名为done.txt, 创建目录dir_a，将done.txt移动到目录dir_a下
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ mkdir dir_a
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ mv task.txt ./dir_a/done.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ ls
dir_a
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Right!
homework_6 is Right!
homework_7 is Wrong.
homework_8 is Wrong.
homework_9 is Wrong.
score: 70/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_6$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_7
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ midir dir_0 dir_1 dir_2
-bash: midir: command not found
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ mkdir dir_0 dir_1 dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ mv a.txt ./dir_0
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cd dir_0       
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_0$ ls
a.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_0$ mv a.txt a0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_0$ ls
a0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_0$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cd ..    
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ homework 1 create 7
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_7
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ mkdir dir_0 dir_1 dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp a.txt ./dir_0/a0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp b.txt ./dir_0/b0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp c.txt ./dir_0/c0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp a.txt ./dir_1/a0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp b.txt ./dir_1/b0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp c.txt ./dir_1/c0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cd dir_1
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ ls
a0.txt  b0.txt  c0.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ mv a0.txt a1.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ mv b0.txt b1.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ mv c0.txt c1.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ ls
a1.txt  b1.txt  c1.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7/dir_1$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp a.txt ./dir_2/a2.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp b.txt ./dir_2/b2.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cp c.txt ./dir_2/c2.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ ls
a.txt  b.txt  c.txt  dir_0  dir_1  dir_2
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Right!
homework_6 is Right!
homework_7 is Right!
homework_8 is Wrong.
homework_9 is Wrong.
score: 80/100
acs@6c70dd798fbe:~/homework/lesson_1/homework_7$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_8
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ ls
dir_a  dir_b  dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ homework 1 show
网页格式地址：https://www.acwing.com/file_system/file/content/whole/index/content/2855530/

1. 常用命令介绍
    (1) ctrl c: 取消命令，并且换行
    (2) ctrl u: 清空本行命令
    (3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
    (4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
    (5) pwd: 显示当前路径
    (6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
    (7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
    (8) mkdir XXX: 创建目录XXX
    (9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
    (10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
    (11) touch XXX: 创建一个文件
    (12) cat XXX: 展示文件XXX中的内容
    (13) 复制文本
        windows/Linux下：Ctrl + insert，Mac下：command + c
    (14) 粘贴文本
        windows/Linux下：Shift + insert，Mac下：command + v

2. 创建作业 & 测试作业的正确性
    homework 1 create 可以重新创建所有lesson_1的作业
    homework 1 create id 可以单独创建lesson_1的第id个作业. e.g.
        homework 1 create 0 可以只重新创建lesson_1的第0个作业
    homework 1 test 可以评测lesson_1的所有作业

3. 作业
    创建好作业后，先进入文件夹/home/acs/homework/lesson_1/，然后：
    (0) 进入homework_0文件夹，分别创建文件夹dir_a, dir_b, dir_c
    (1) 进入homework_1文件夹，将a.txt, b.txt, c.txt 分别复制成: a.txt.bak, b.txt.bak, c.txt.bak
    (2) 进入homework_2文件夹，将a.txt, b.txt, c.txt 分别重命名为: a_new.txt, b_new.txt, c_new.txt
    (3) 进入homework_3文件夹，将dir_a文件夹下的a.txt, b.txt, c.txt分别移动到文件夹dir_b下
    (4) 进入homework_4文件夹，将普通文件a.txt, b.txt, c.txt删除
    (5) 进入homework_5文件夹，将文件夹dir_a, dir_b, dir_c删除
    (6) 进入homework_6文件夹，查看task.txt的内容，并按其指示进行操作
    (7) 进入homework_7文件夹，创建文件夹dir_0, dir_1, dir_2，
        将a.txt, b.txt, c.txt复制到dir_0下，重命名为a0.txt, b0.txt, c0.txt;
        将a.txt, b.txt, c.txt复制到dir_1下，重命名为a1.txt, b1.txt, c1.txt;
        将a.txt, b.txt, c.txt复制到dir_2下，重命名为a2.txt, b2.txt, c2.txt;
    (8) 进入homework_8文件夹，分别在dir_a, dir_b, dir_c文件夹下查看task.txt的内容，并分别按照指示进行操作
    (9) 进入homework_9文件夹，将其中所有txt类型的文件删除
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ cd homework_8
-bash: cd: homework_8: No such file or directory
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ ls         
dir_a  dir_b  dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ cd dir_a
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_a$ ls
a.txt  task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_a$ cat task.txt
将a.txt删除
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_a$ rm a.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_a$ ls
task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_a$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ cd dir_b
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_b$ ls
b.txt  task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_b$ cat task.txt
将b.txt重命名为b_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_b$ mv b.txt b_new.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_b$ ls
b_new.txt  task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_b$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ ls
dir_a  dir_b  dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ cd dir_c
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_c$ ls
c.txt  task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_c$ cat task.txt
将c.txt复制成c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_c$ cp c.txt c.txt.bak
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_c$ ls
c.txt  c.txt.bak  task.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_8/dir_c$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1/homework_8$ cd ..
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Right!
homework_6 is Right!
homework_7 is Right!
homework_8 is Right!
homework_9 is Wrong.
score: 90/100
acs@6c70dd798fbe:~/homework/lesson_1$ cd homework_9
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ ls
file_0.dmg   file_12.dmg  file_16.dmg  file_2.doc   file_23.txt  file_27.txt  file_4.dmg  file_8.dmg
file_1.ppt   file_13.ppt  file_17.ppt  file_20.dmg  file_24.dmg  file_28.dmg  file_5.ppt  file_9.ppt
file_10.doc  file_14.doc  file_18.doc  file_21.ppt  file_25.ppt  file_29.ppt  file_6.doc
file_11.txt  file_15.txt  file_19.txt  file_22.doc  file_26.doc  file_3.txt   file_7.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ rm /*
rm: cannot remove '/bin': Permission denied
rm: cannot remove '/boot': Is a directory
rm: cannot remove '/dev': Is a directory
rm: cannot remove '/etc': Is a directory
rm: cannot remove '/home': Is a directory
rm: cannot remove '/lib': Permission denied
rm: cannot remove '/lib32': Permission denied
rm: cannot remove '/lib64': Permission denied
rm: cannot remove '/libx32': Permission denied
rm: cannot remove '/media': Is a directory
rm: cannot remove '/mnt': Is a directory
rm: cannot remove '/opt': Is a directory
rm: cannot remove '/proc': Is a directory
rm: cannot remove '/root': Is a directory
rm: cannot remove '/run': Is a directory
rm: cannot remove '/sbin': Permission denied
rm: cannot remove '/srv': Is a directory
rm: cannot remove '/sys': Is a directory
rm: cannot remove '/tmp': Is a directory
rm: cannot remove '/usr': Is a directory
rm: cannot remove '/var': Is a directory
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ rm .*
rm: cannot remove '.': Is a directory
rm: cannot remove '..': Is a directory
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ rm -rf .txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ ls
file_0.dmg   file_12.dmg  file_16.dmg  file_2.doc   file_23.txt  file_27.txt  file_4.dmg  file_8.dmg
file_1.ppt   file_13.ppt  file_17.ppt  file_20.dmg  file_24.dmg  file_28.dmg  file_5.ppt  file_9.ppt
file_10.doc  file_14.doc  file_18.doc  file_21.ppt  file_25.ppt  file_29.ppt  file_6.doc
file_11.txt  file_15.txt  file_19.txt  file_22.doc  file_26.doc  file_3.txt   file_7.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ rm *.txt
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ ls
file_0.dmg   file_12.dmg  file_16.dmg  file_2.doc   file_22.doc  file_26.doc  file_4.dmg  file_8.dmg
file_1.ppt   file_13.ppt  file_17.ppt  file_20.dmg  file_24.dmg  file_28.dmg  file_5.ppt  file_9.ppt
file_10.doc  file_14.doc  file_18.doc  file_21.ppt  file_25.ppt  file_29.ppt  file_6.doc
acs@6c70dd798fbe:~/homework/lesson_1/homework_9$ cd ..    
acs@6c70dd798fbe:~/homework/lesson_1$ ls
homework_0  homework_2  homework_4  homework_6  homework_8
homework_1  homework_3  homework_5  homework_7  homework_9
acs@6c70dd798fbe:~/homework/lesson_1$ homework 1 test
homework_0 is Right!
homework_1 is Right!
homework_2 is Right!
homework_3 is Right!
homework_4 is Right!
homework_5 is Right!
homework_6 is Right!
homework_7 is Right!
homework_8 is Right!
homework_9 is Right!
score: 100/100
```

涉及到的知识点：

```bash
cp name_1 name_2  # 将name_1文件拷贝并且命名为name_2
mv name_1 name_2  # 将name_1文件移动并且命名为name_2
mkdir name_1  # 创建名为name_1的文件或者文件夹
cd name_1  # 进入名为name_1的文件夹中
rm name_1  # 删除名为name_1的文件
rm -rf name_1  # 删除名为name_1的文件夹
rm *.txt  # 删除当前文件夹之下所有后缀为txt的文件
./  # 表示当前文件夹开始的路径
pwd  # 显示当前文件夹的路径
cat name_1  # 将name_1文件打印出来
```
