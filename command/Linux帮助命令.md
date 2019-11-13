# Linux帮助命令

- man命令
- help命令
- info命令



------



#### man命令

`man`是manual的缩写。通常用于获取某个命令的使用说明。

格式：

```
man 命令
```

示例，获取man命令的第7章的帮助信息：

```shell
[root@localhost ~]# man 7 man
```



------



#### help命令

`help`可以获取帮助信息。

shell（命令解释器）自带的命令称为内部命令，其他命令称为外部命令。

判断是一个命令是否是内部命令，可以使用`type`命令查看，如下：

```shell
[root@localhost ~]# type cd
cd 是 shell 内嵌
[root@localhost ~]# type ls
ls 是 `ls --color=auto' 的别名
```

内部命令可以通过`help`命令获取帮助信息。

```
help 命令
```

外部命令使用`--help`选项获取帮助信息：

```
命令 --help
```

示例一，通过`help`命令查看`cd`（内部命令）的帮助信息：

```shell
[root@localhost ~]# help cd
cd: cd [-L|[-P [-e]]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
...
```

示例二，通过`--help`选项查看`ls`（外部命令）的帮助信息：

```shell
[root@localhost ~]# ls --help
用法：ls [选项]... [文件]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.
...
```



------



#### info命令

`info`命令是`help`命令的补充，可以显示更加具体的帮助信息。

格式：

```
info 命令
```

