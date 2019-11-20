# Linux用户身份操作命令

- useradd



------



#### useradd命令

useradd命令用于创建新的用户。

格式：

```
useradd [选项] 用户名
```

说明：

使用useradd命令创建用户账户时，默认的用户家目录会被存放在/home目录中，默认的Shell解释器为/bin/bash，而且默认会创建一个与该用户同名的基本用户组。

useradd命令中的选项说明：

- `-d`：指定用户的家目录（默认为/home/username）
- `-e`：账户的到期时间，格式为YYYY-MM-DD
- `-u`：指定该用户的默认UID，由管理员创建的普通用户的UID默认是从1000开始的（即使前面有闲置的号码）。（root管理员UID为0，系统用户UID为1～999，Linux系统为了避免因某个服务程序出现漏洞而被黑客提权至整台服务器，默认服务程序会有独立的系统用户负责运行，进而有效控制被破坏范围。）
- `-g`：指定一个初始的用户基本组（必须已存在）（在Linux系统中创建每个用户时，将自动创建一个与其同名的基本用户组，而且这个基本用户组只有该用户一个人。）
- `-G`：指定一个或多个扩展用户组。（如果该用户以后被归纳入其他用户组，则这个其他用户组称之为扩展用户组。一个用户只有一个基本用户组，但是可以有多个扩展用户组。）
- `-N`：不创建与用户同名的基本用户组。
- `-s`：指定该用户的默认Shell解释器。

示例一，创建一个普通用户wynologin，并指定家目录的路径为/home/wynologin、用户的UID为8888，以及Shell解释器为/sbin/nologin：

```shell
[root@localhost ~]# useradd -d /home/wynologin -u 8888 -s /sbin/nologin wynologin
[root@localhost home]# id wynologin
uid=8888(wynologin) gid=8888(wynologin) 组=8888(wynologin)
```

注意：/sbin/nologin解释器与Bash解释器完全不同，一旦用户的解释器被设置为nologin，则代表该用户不能登录到系统中。（因为登录系统使用的是Bash解释器）



------



#### groupadd命令

文字描述

格式：



