# Linux
linux常用命令的学习


#ls命令 – 显示指定工作目录下的内容及属性信息
语法格式: ls [选项] [文件]
常用参数：
      -a	显示所有文件及目录 (包括以“.”开头的隐藏文件)
      -l	使用长格式列出文件及目录信息
      -r	将文件以相反次序显示(默认依英文字母次序)
      -t	根据最后的修改时间排序
      -A	同 -a ，但不列出 “.” (当前目录) 及 “..” (父目录)
      -S	根据文件大小排序
      -R	递归列出所有子目录




#cat命令 – 在终端设备上显示文件内容
语法格式：cat [参数] [文件]
常用参数：
      -n	显示行数（空行也编号）
      -s	显示行数（多个空行算一个编号）
      -b	显示行数（空行不编号）
      -E	每行结束处显示$符号
      -T	将TAB字符显示为 ^I符号
      -v	使用 ^ 和 M- 引用，除了 LFD 和 TAB 之外
      -e	等价于”-vE”组合
      -t  等价于”-vT”组合
      -A	等价于 -vET组合
      --help	显示帮助信息
      --version	显示版本信息


#cp命令 – 复制文件或目录
语法格式：cp [参数] [文件]
常用参数：
      -f	若目标文件已存在，则会直接覆盖原文件
      -i	若目标文件已存在，则会询问是否覆盖
      -p	保留源文件或目录的所有属性
      -r	递归复制文件和目录
      -d	当复制符号连接时，把目标文件或目录也建立为符号连接，并指向与源文件或目录连接的原始文件或目录
      -l	对源文件建立硬连接，而非复制文件
      -s	对源文件建立符号连接，而非复制文件
      -b	覆盖已存在的文件目标前将目标文件备份
      -v	详细显示cp命令执行的操作过程
      -a	等价于“dpr”选项
      
      
      
#mkdir命令 – 创建目录
语法格式 : mkdir [参数] [目录]
常用参数：
      -p	递归创建多级目录
      -m	建立目录的同时设置目录的权限
      -z	设置安全上下文
      -v	显示目录的创建过程
      
      
#echo命令 – 输出字符串或提取Shell变量的值
语法格式：echo [参数] [字符串]
常用参数：
    -n	不输出结尾的换行符
    -e “\a”	发出警告音
    -e “\b”	删除前面的一个字符
    -e “\c”	结尾不加换行符
    -e “\f”	换行，光标扔停留在原来的坐标位置
    -e “\n”	换行，光标移至行首
    -e “\r”	光标移至行首，但不换行
    -E	禁止反斜杠转移，与-e参数功能相反
    —version	查看版本信息
    --help	查看帮助信息



#mv命令 – 移动或改名文件
语法格式：mv [参数]

常用参数：

    -i	若存在同名文件，则向用户询问是否覆盖
    -f	覆盖已有文件时，不进行任何提示
    -b	当文件存在时，覆盖前为其创建一个备份
    -u
    当源文件比目标文件新，或者目标文件不存在时，才执行移动此操作
    
    
    
#rm命令 – 移除文件或目录
语法格式：rm [参数] [文件]
常用参数：
  -f	忽略不存在的文件，不会出现警告信息
  -i	删除前会询问用户是否操作
  -r/R	递归删除
  -v	显示指令的详细执行过程


#pwd命令 – 显示当前路径
语法格式: pwd [参数]
常用参数：

  -L	显示逻辑路径



#ssh命令 – 安全连接客户端
语法格式: ssh [参数] [远程主机]

常用参数：
  -1	强制使用ssh协议版本1
  -2	强制使用ssh协议版本2
  -4	强制使用IPv4地址
  -6	强制使用IPv6地址
  -A	开启认证代理连接转发功能
  -a	关闭认证代理连接转发功能
  -b<IP地址>	使用本机指定的地址作为对位连接的源IP地址
  -C	请求压缩所有数据
  -F<配置文件>	指定ssh指令的配置文件，默认的配置文件为“/etc/ssh/ssh_config”
  -f	后台执行ssh指令
  -g	允许远程主机连接本机的转发端口
  -i<身份文件>	指定身份文件（即私钥文件）
  -l<登录名>	指定连接远程服务器的登录用户名
  -N	不执行远程指令
  -o<选项>	指定配置选项
  -p<端口>	指定远程服务器上的端口
  -q	静默模式，所有的警告和诊断信息被禁止输出
  -X	开启X11转发功能
  -x	关闭X11转发功能
  -y	开启信任X11转发功能



#df命令 – 显示磁盘空间使用情况
语法格式： df [参数] [指定文件]

常用参数：
  -a	显示所有系统文件
  -B <块大小>	指定显示时的块大小
  -h	以容易阅读的方式显示
  -H	以1000字节为换算单位来显示
  -i	显示索引字节信息
  -k	指定块大小为1KB
  -l	只显示本地文件系统
  -t <文件系统类型>	只显示指定类型的文件系统
  -T	输出时显示文件系统类型
  -- -sync	在取得磁盘使用信息前，先执行sync命令



#rpm命令 – RPM软件包管理器
概括的说，rpm命令包含了五种基本功能：安装、卸载、升级、查询和验证。
语法格式：rpm [参数] [软件包]

常用参数：
  -a	查询所有的软件包
  -b或-t	设置包装套件的完成阶段，并指定套件档的文件名称；
  -c	只列出组态配置文件，本参数需配合”-l”参数使用
  -d	只列出文本文件，本参数需配合”-l”参数使用
  -e或--erase	卸载软件包
  -f	查询文件或命令属于哪个软件包
  -h或--hash	安装软件包时列出标记
  -i	显示软件包的相关信息
  --install	安装软件包
  -l	显示软件包的文件列表
  -p	查询指定的rpm软件包
  -q	查询软件包
  -R	显示软件包的依赖关系
  -s	显示文件状态，本参数需配合”-l”参数使用
  -U或--upgrade	升级软件包
  -v	显示命令执行过程
  -vv	详细显示指令执行过程


#tail命令 – 查看文件尾部内容
语法格式：tail [参数]

常用参数：
    --retry	即是在tail命令启动时，文件不可访问或者文件稍后变得不可访问，都始终尝试打开文件。使用此选项时需要与选项“——follow=name”连用

    -c<N>或——bytes=<N>	输出文件尾部的N（N为整数）个字节内容

    -f<name/descriptor>	--follow<nameldescript>：显示文件最新追加的内容

    -F	与选项“-follow=name”和“--retry”连用时功能相同

    -n<N>或——line=<N>	输出文件的尾部N（N位数字）行内容

    --pid=<进程号>	与“-f”选项连用，当指定的进程号的进程终止后，自动退出tail命令

    --help	显示指令的帮助信息

    --version	显示指令的版本信息


#mount命令 – 文件系统挂载
mount命令用于加载文件系统到指定的加载点。此命令的最常用于挂载cdrom，使我们可以访问cdrom中的数据，因为你将光盘插入cdrom中，Linux并不会自动挂载，必须使用Linux mount命令来手动完成挂载。
语法格式：mount [参数]

常用参数：﻿
    -t	指定挂载类型
    -l	显示已加载的文件系统列表
    -h	显示帮助信息并退出
    -V	显示程序版本
    -n	加载没有写入文件“/etc/mtab”中的文件系统
    -r	将文件系统加载为只读模式
    -a	加载文件“/etc/fstab”中描述的所有文件系统



#tftp命令 – 上传及下载文件
tftp命令用于传输文件。ftp让用户得以下载存放于远端主机的文件，也能将文件上传到远端主机放置。
tftp是简单的文字模式ftp程序，它所使用的指令和ftp类似。
语法格式：tftp [参数]
常用参数：
    connect	连接到远程tftp服务器
    mode	文件传输模式
    put	上传文件
    get	下载文件
    quit	退出
    verbose	显示详细的处理信息
    trace	显示包路径
    status	显示当前状态信息
    binary	二进制传输模式
    ascii	ascii 传送模式
    rexmt	设置包传输的超时时间
    timeout	设置重传的超时时间
    help	帮助信息
    ?	帮助信息

#
#
#
#
#















