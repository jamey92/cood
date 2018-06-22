基本操作

```
adduser 创建用户名
passwd 修改密码
who 获取登录信息
whoami / who am i  查看自己
clear 清屏
ps  显示瞬间进程
logout 退出
uname 查看系统  hostname 主机名
whereis / which 用于查找文件
man / info 查看帮助
su 切换用户  sudo 以管理员身份执行
userdel 删除用户
wget(跟链接) 下载
pwd - print working directory 显示当前所在工作目录的全路径
ps -ef | grep 程序名 查看某个程序进程
```

文件和文件夹操作

```
usr 目录 文件系统 etc目录 系统、软件配置
ctrl + c 终止命令
ctrl + z 任务放到后台运行
ls - list directory contents
	ls -l 长格式
	ls -a 查看所有文件/文件夹(包括隐藏)
	ls -R 递归显示
	ls -r 反转
.bash_profile 系统的每个用户设置环境信息,当用户第一次登录时,该文件被执行.
mkdir - make directory 创建文件夹
rmdir 删除空文件夹
touch 文件不存在创建文件，存在时修改时间戳
rm - remove 既可以删除文件又可以删除文件夹
	rm -r 递归删除
	rm -i 删除已有文件或目录之前先询问用户
	rm -f 强制删除，不询问用户
cp 复制  scp 安全复制
mv 剪切
history 查找历史记录
	
lost+found目录 损毁文件，删除文件(能够恢复)
查看文件内容 cat / head / tail
	cat 打印文件所有内容
	head -n(数字 指定行数) 显示前几行
	tail -n(数字 指定行数) 显示最后几行
| 管道  > 输出重定向 >> 追加输出重定向  2> 错误输出重定向
grep 文本搜索工具，能够使用正则表达式 
	cat 文件名 | grep '<div .*>'
	grep '<div .*>' -R(递归) -n(行号) >(输出重定向) result.txt 2>(错误重定向) error.txt &(后台执行)
find -name(目录名) 在指定目录下查找文件
```



```
时间和空间是不可调和的矛盾
硬件和软件在逻辑上是等效的
yum - yellwodog updater modified 包管理工具
	yum install 软件名 安装软件
	yum search
rpm 安装与卸载
	-i 安装 vm显示安装
	-qa 查询所有  rpm -qa | grep 软件名  查询是否安装成功
	-e 需要卸载的安装包

软件名 --version 查看软件信息
jobs 任务列表以及任务状态
	fg %x 放回到前台执行 x 任务编号
	bg %x 放回到后台执行
top 实时动态查看系统的整体运行状态
wc - word count 数单词数和行数
diff 比较给定的两个文件不同
file 分析文件类型
sort 文件排序
echo 输出 打印
ln 创建链接 硬链接不占用空间(备份) ln foo3.html ~/foo.html
	ln -s 软连接(相当于快捷方式)  ln -s 文件位置 快捷链接位置
		ln -s /usr/local/python3.6/bin/ipython3 /usr/bin/ipython3

第一个 - l 链接 r 文件 d 文件夹
rw - 文件的所有者 r-- 同组用户 r--其他用户
rwx              rwx          rwx
111(二进制)      110          110
7                6            6
rwx              rwx          rwx
111(二进制)      110          110
7                6            6
chomd 变更文件或目录的权限 u+x
chmod 777 guess.py
chmod 766 guess.py
```

压缩与解压

```
tar 归档与解归档 想要压缩一大堆文件时，得先将这一大堆文件先打成一个包（tar命令），然后再用压缩程序进行压缩
	-xvf 解归档
	-cvf 归档
gunzip 解压缩 解压的扩展名.gz
gzip 压缩
xz 压缩与解压
	-z 压缩 压缩比 -0~-9
	-d 解压缩
```

vim编辑器

```
编辑
dd 删除一行  yy 复制一行
ctrl + r 还原
G 到末尾  gg 到第一行 XG 到第几行
ctrl + f / b  后翻一页/ 前翻一页
: w/q/q! 保存/退出/强退

```

HTTP

```
MySQL/ Redis/ Nginx
DNS - 域名解析成IP地址
HTTP服务器 - 
Apache  LAMP = Linux + Apache + MySQL + PHP
Nginx   LNMP = Linux + Nginx + MySQL + Python
ps -aux 查看进程 ps -aus | grep nginx
kill 杀进程 -9 强行关掉
netstat 打印网络连接，路由表，接口统计信息，查看端口号
	netstat -nap | grep 80

systemctl stop/ start 停服务/ 启动服务 server firewalls start 启动 Firewalls(防火墙)服务
firewall -cmd 
systemctl status 查看状态
mysql -u root -p
systemctl enable / disable 开机自启/ 禁止自启
！ifconfig 查看内网ip
redis-server myredis.conf > myredis.log & 静默启动服务器，把内容保存在myredis.log 文件中
Filter(过滤) - Map - Reduct(规约 多条合并为一条)
```

