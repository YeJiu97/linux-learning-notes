# 03 - Getting Help

## Get Help

如果我不确定某一个指令是怎么用的，可以使用man指令来调查：

```bash
CAL(1)                                       BSD General Commands Manual                                       CAL(1)

NAME
     cal, ncal — displays a calendar and the date of Easter

SYNOPSIS
     cal [-3hjy] [-A number] [-B number] [[month] year]
     cal [-3hj] [-A number] [-B number] -m month [year]
     ncal [-3bhjJpwySM] [-A number] [-B number] [-W number] [-s country_code] [[month] year]
     ncal [-Jeo] [-A number] [-B number] [year]
     ncal [-CN] [-H yyyy-mm-dd] [-d yyyy-mm]

DESCRIPTION
     The cal utility displays a simple calendar in traditional format and ncal offers an alternative layout, more op‐
     tions and the date of Easter.  The new format is a little cramped but it makes a year fit on a 25x80 terminal.
     If arguments are not specified, the current month is displayed.

     The options are as follows:

     -h      Turns off highlighting of today.

     -J      Display Julian Calendar, if combined with the -o option, display date of Orthodox Easter according to
             the Julian Calendar.

     -e      Display date of Easter (for western churches).

     -j      Display Julian days (days one-based, numbered from January 1).

     -m month
```

这个是：

```bash
man ncal
```

的结果。

同样的，我们可以查看date之类的结果：

```bash
DATE(1)                                             User Commands                                             DATE(1)

NAME
       date - print or set the system date and time

SYNOPSIS
       date [OPTION]... [+FORMAT]
       date [-u|--utc|--universal] [MMDDhhmm[[CC]YY][.ss]]

DESCRIPTION
       Display the current time in the given FORMAT, or set the system date.

       Mandatory arguments to long options are mandatory for short options too.

       -d, --date=STRING
              display time described by STRING, not 'now'

       --debug
              annotate the parsed date, and warn about questionable usage to stderr

       -f, --file=DATEFILE
              like --date; once for each line of DATEFILE

       -I[FMT], --iso-8601[=FMT]
              output date/time in ISO 8601 format.  FMT='date' for date only (the default), 'hours', 'minutes', 'sec‐
              onds', or 'ns' for date and time to the indicated precision.  Example: 2006-08-14T02:34:56-06:00

       -R, --rfc-email
              output date and time in RFC 5322 format.  Example: Mon, 14 Aug 2006 02:34:56 -0600
```

![Untitled](03%20-%20Getting%20Help%2027656beed72c461c824dec35ec34d7c3/Untitled.png)

我们可以使用一下给出来的提示：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ ncal -d 1969-08
    August 1969
Su     3 10 17 24 31
Mo     4 11 18 25
Tu     5 12 19 26
We     6 13 20 27
Th     7 14 21 28
Fr  1  8 15 22 29
Sa  2  9 16 23 30
```

## type 和 which

使用type来查看一下：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ type clear
clear is hashed (/usr/bin/clear)
```

usr之下的bin中，bin是binary的缩写，这意味着clear是可执行文件。

接着是查看一下cd：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ type cd
cd is a shell builtin
```

从结果来看，cd不是一个binary可执行文件，而是一个shell函数。

which的逻辑和type是类似的。

## help指令

我们可以测试一下cd：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.

    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.

    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.

    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.

    Options:
      -L        force symbolic links to be followed: resolve symbolic
                links in DIR after processing instances of `..'
      -P        use the physical directory structure without following
                symbolic links: resolve symbolic links in DIR before
                processing instances of `..'
      -e        if the -P option is supplied, and the current working
                directory cannot be determined successfully, exit with
                a non-zero status
      -@        on systems that support it, present a file with extended
                attributes as a directory containing the file attributes

    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.

    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
```

## 其他

如果要知道自己是谁，或者说这个账户是谁，可以使用whoami：

```bash
yejiu97@DESKTOP-S9ODFEQ:/mnt/c/Users/yinia/Desktop/WSL/03$ whoami
yejiu97
```