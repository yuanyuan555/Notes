# 配置　vim
## 配置前需要先安装　vim
#### 解压　vimconfig.rar  后会有一个 vimconfig 的文件夹
    cd vimconfig
    sudo bash ./config.sh

# linux  命令

## ifconfig 　:　 查看IP

#### linux@ 　 :　 @ 前是用户名
#### ～　　：　　主目录
#### ls  　:　 查看当前目录中的文件
#### ls -a 　:　 查看隐藏文件，　　以 . 开头的是隐藏文件
#### ls -l 　: 　查看详细信息
#### ls -a -l  =  ls -al  ： 查看所有目录的详细信息
    drwxr-xr-x　　　　　　　6　　　　　　bao　　　　　　bao 　　　　4096　　　10月 27 14:17 　　　　桌面
    文件类型，文件权限　 硬链接个数　　　用户名　　     　组　　　　　大小　　　最新修改的时间
#### cd  　:　　切换目录　　
#### cd + 回车　　：　回到家目录
#### ctrl　+ l 　:　清空
#### 基本文件的操作
#### touch 　:　　创建文件
#### cp 　　复制的原文件的路径　　要复制到的那里去　:　复制
#### mv 　原文件名　　　新文件名/目录名　　: 重命名，移动
#### rm 　: 　删除
#### .　　　　　:　当前目录
#### . .　　      ：上一级目录

#### pwd  　: 　输出你当前所在路径的绝对路径
#### cat 　:　　列出当前文件的内容
#### man 需要查的命令　　:　 　查找某个命令的手册

#### mkdir　 :　 创建目录
#### cp 原文件　目录　-a : 　复制目录加　-a
#### mv 
#### rm  删除文件名　-rf　 :　 删除文件　　　-rf　 ：　强制删除

# 压缩　解压
#### gzip  文件名　: 压缩文件   (只能压缩文件)
#### gunzip  文件包　：　解压文件
#### bzip2   文件名　:　压缩文件　　(只能压缩文件
#### bunzip2  文件名 :　解压 文件
#### tar  文件名/目录名　：　压缩　/　解压
#### tar 　-czvf   压缩后的文件名　 要压缩的文件名　（gz 格式）
#### tar  -xzvf   解压文件名
#### tar 　-cjvf   压缩后的文件名　 要压缩的文件名　（bz2 格式）
#### tar  -xjvf   解压文件名
#### tar -cJvf   压缩后的文件名　 要压缩的文件名　（xz 格式）
#### tar -xvf 　 解压文件名　（什么格式都可以解压）

# vim 的基本使用
    i  ：在当前字符的左边插入
    I  ：在当前行首插入
    a  ：在当前字符的右边插入
    A  ：在当前行尾插入
    o  ：在当前行下面插入一个新行
    O  ：在当前行上面插入一个新
    h  : 向前移动一个字符
    j  : 向上移动一行
    k  : 向下移动一行
    l  : 向后移动一个字符
    yy : 复制当前一行
    dd :剪切当前一行
    p  : 粘贴内容到游标之后
    P  : 粘贴内容到游标之前
    u  ：　撤销

# shell通配符
#### * 号用于任意长度字符　　　例：ls *   
#### ? 号用于匹配任意一个字符　例：ls file_?  　　有几个　？　就匹配几个字符
#### [] 号用于制定匹配字符    例：ls file_[0123]  或　ls file_[0-3] 只匹配　[]　内带有　０，１，２，３的文件
#### ^ 号用于[]中进行字符过滤　例：ls file_[^123]  匹配除了带有　１，２，３　的所有文件
    
# etc 配置文件
#### 添加新用户
#### adduser 新的用户名 ：添加新用户  （注：仔细观看记住密码，看清是什么密码）
#### vim /etc/passwd      查看配置文件的...
#### vim /etc/group       查看配置文件的组
#### usermod -s/bin/bash  -G group,group  newuser  
    修改解释器                   组           目录
    -G 修改用户所属的附加群组　
#### gpasswd -a 添加用户到组
#### gpasswd -d 删除 组里的用户
# root 超级用户
#### sudo root password   超级用户密码
#### deluser newuser --remove-home     删除用户  （连带主目录一起删除）
#### delgroup newgroup   删除组名
	注：如果删除了用户　ls 查看普通用户已经删除，但是电脑仍然有你删的用户，那么说明
	你没有“退出”要删除的用户。而是切换出了该用户。需要回到要删除而没有删除的用户。重
	新“退出”该用户，再进行删除。

#### id  列出当前
## 先删用户 后删组
#### 给普通用户赋予超级用户权限的方法 vi /etc/su
	vi /etc/sudoers
	然后再修改问       
	# User privilege specification
	root  ALL=(ALL:ALL)ALL
	....  ALL=(ALL:ALL)ALL
	....代表你要赋予权限的不同用户名
#### shutdown -f now 现在重启
		-h     现在关机
		-k     通知关机
#### shutdown -c  取消之前关机重启等命令   

#### df       扫描磁盘的使用情况
#### df -h    人类可读的磁盘使用情况
        -a　　包含所有的具有０ Block的文件系统
        -T    显示文件系统的形式
#### du       估计文件使用了多少磁盘空间
#### du -h    以　K , M , G 为单位，提高信息的可读性
        -s    直接统计结果不显示信息
#### ps       系统最近运行的
#### ps ajx   列出当前系统上前后台运行的程序

#### pstree　　命令将所有行程以树状图显示

#### top　用于实现显示process的动态

### kill 杀死
#### kill -9 进程ID号  : 结束一个进程
#### ps ajx  :  查看ID号


### 程序:程序是静态的，存在磁盘上的
### 进程：处于运行状态的程序

# linux 中的软件包管理机制
### Deb 软件包的基本操作
###### 例：sl_3.03-17_amd64.deb
	sl,表示软件包名称
	3.03-17, 表示版本号和修订版本号
	amd64 ,表示运行机器的平台框架（64位）　　x86 ：　３２位
	deb, 表示deb软件包的后缀名

# 在超级用户下安装卸载
## 本地安装　：
	dpkg      : 本地安装操作命令
	dpkg -i 软件报的全程　:　软件包安装
	dpkg -s 包名　：　查看软件包的安装状态
	dpkg -L 包名　：　查看软件包安装的路径
	dpkg -P 包名　：　卸载　（彻底卸载，移除所有的配置文件）
	dpkg -r 包名　：　软件包卸载
	dpkg -get-selections : 列出所有安装的软件包
## 在线安装　：  
	apt-get update : 更新本地软件包（源）
	apt-get install 安装包的名字　：　安装
	apt-cache policy 软件包　：　查看软件包的安装状态
	apt-cache show 软件包　：　查看信息
	apt-get remove --purge 软件包　：　卸载　（配置文件一起删除）
	apt-get download 软件包　：　只下载包不安装
	apt-get source 软件包　：　下载源码
	apt-get upgrade : 升级软件包
### 如果安装失败。输入以下命令进行调节，解决依赖关系后继续安装
	sudo apt-get install -f

### FTP(简单文件传输协议)服务器和用户的安装
###### １．检查TFTP服务器和客户端的安装状态
	dpkg -s tftpd-hpa
	dpkg -s tftp-hpa
###### ２．在线安装服务器和客户端
	sudo apt-get update
	sudo apt-get install tftpd-hpa
	sudo apt-get install tftp-hpa
### TFTP服务器的配置
###### 修改TFTP服务器的配置文件　/etc/default/tftpd-hpa
	TFTP_USERNAME="tftp"
	TFTP_DIRECTORY="/var/lib/tftpboot"
	TFTP_ADDRESS="[::]:69"
	TFTP_OPTIONS="--SECURE  -c  -l"
## TFTP服务的启动，重启以及停止操作
#### 启动服务
	root@linux:~# service tftpd-hpa start
	tftpd-hpa start/running,process 5061
#### 重启服务
	root@linux:~# service tftpd-hpa restart
	tftpd-hpa stop/waiting
	tftpd-hpa start/running,process 5096
#### 停止服务
	root@linux:~# service tftpd-hpa stop
	tftpd-hpa stop/waiting
## TFTP服务的测试
#### 1.客户端连接服务器
	bao@linux:~$ tftp 127.0.0.1
	tftp>
#### 2.输入上传文件命令
	bao@linux:~$ tftp 127.0.0.1
	tftp> put 文件名
#### 3.输入下载文件命令
	bao@linux:~$ tftp 127.0.0.1
	tftp>　get 文件名
#### 4.输入退出命令
	bao@linux:~$ tftp 127.0.0.1
	tftp>　quit
	
# NFS服务器的安装
#### 1.检查NFSf服务器的安装状态
	dpkg -s nfs-kernel-server
#### 2.在线安装NFS服务器
	sudo apt-get update
	sudo apt-get install nfs-kernel-server
## NFS服务器的配置
##### 修改NFS服务器的配置文件　/etc/exports 文件
	# /etc/exports: the access control list for filesystems which may be exported
	#	to NFS clients. See exports(5)
	#
	# Example for NFSv2 and NFSV3:
	# /srv/home  hostname1(rw,sync,no_subtree_check) hostname2(ro,sync,no_subtree_check)
	#
	# Eeample for NFSv4:
	# /srv/nfs4         gss/krb5i(rw,sync,fsid=0,crossmnt,no_subtree_check)
	# /srv/nfs4/homes   gss/krb5i(rw,sync,no_subtree_check)
	# 
	/nfs_root_dir   *(rw,sync,no_subtree_check,no_root_squash)
### 配置详细参数可以参考　man exports 手册
## NFS　服务的启动，重启以及停止操作
#### 启动服务
	root@linux:/# service nfs-kernel-server start
#### 重新启动
	root@linux:/# service nfs-kernel-server restart
#### 停止启动
	root@linux:/# service nfs-kernel-server stop

### NFS 服务的测试
#### 1. 客户端创建一个挂在目录
	mkdir  /mount_nfs
#### 2. 客户端挂在远端ＮＦＳ服务器
	root@linux:/# mount -t nfs 127.0.0.1:/nfs_root_dir   /mount_nfs
#### 3.挂在成功后操作本地的　mount_nfs 目录就相当于操作远端 nfs_root_dir 目录了
### umount mount_nfs/   取消挂载
	
#### 端口号 ： 是用来区分进程的

## 远程安全登录服务器SSH
#### SSH服务器和客户端的安装
###### 1.检查SSH服务器和客户端的安装状态
	dpkg -s openssh-server
	dpkg -s openssh-client
###### 2.在线安装服务器和客户端
	sudo apt-get update
	sudo apt-get install openssh-server
	sudo apt-get install openssh-client
## SSH 服务器的配置
#### 修改SSH服务器的配置文件 /etc/ssh/sshd_config
	配置文件无改动 或者根据自己需要改动 （如无特殊情况不要改动）
##### 重要参数
	port 设置sshd监听的端口号
	ListenAddress 设置sshd 服务器绑定的IP地址
	HostKey 设置包含计算机私人秘钥的文件
	ServerKeyBits 定义服务器秘钥的位数
	LoginGraceTime 设置如果洪湖不能成功登录，在切断连接之前服务器需要等待的时间（以秒为单位）。
	KeyRegenerationInterval 设置再多爱好秒之后自动重新生成服务其的密钥（如果使用密钥）。重新生成密钥是为了防止盗用密钥解密被截获的信息。
	PermitRootLogin 设置 root 能不能用 ssh 登录。这个选项一定不要设成 yes 。
	X11Forwarding 设置是否允许 X11 转发
##### 更多参数参考 man sshd_config 手册

### SSH 服务的启动，重启，及停止操作 （需在超级用户下操作）
	service sshd start	: 启动
	service sshd restart	: 重启
	service sshd stop	: 停止
## SSH 服务的测试
#### 直接使用 ssh 连接主机即可
	root@linux:~# ssh bao@192.168.1.101
	exit 退出连接
### ps ajx | grep 查找的字符串关键字    ：查找字符串
	|  ：  是管道
### ls | wc -l :
	wc : 输出行，单词字节的个数
	-l : 直接输出行
### wc 文件名 ： 查看一个文件的行，单词，字节

### grep : 检索文件内容 ：根据内容找到关键字
### grep 关键字 文件  ： 在文件中找到有关键字的行
### grep -n 关键字  文件 ： 查找的关键字在哪一行
### grep -R 关键字  文件 ： 

#### tree： 列出目录机器文件夹

# scp 拷贝
### scp google-chrome-stable_current_amd64.deb  teacher@192.168.1.98:　　拷贝文件
	scp 文件名  需要拷贝到的路径地址
	scp  bao@192.168.1.101:/home/bao/atom-amd64.deb   .
		是把用户bao 的这个路径下atom复制到自己的当前目录
	： 是路径分隔符
### scp -r ... 拷贝目录（需参数 -r）

## apache (阿帕奇) 的安装及应用
	sudo apt-get install tasksel
	su -                    进入超级用户
	tasksel
	exit                    退出超级用户
	ps ajx | grep apache
	cd /var/www
	sudo chmod 777 html
	cd html
	mkdir download
	cd download
	网页输入IP 192.168.1.101/download    就能实现在download下载的功能了（IP根据电脑的IP进行改动）
	
	
	
	
	
















