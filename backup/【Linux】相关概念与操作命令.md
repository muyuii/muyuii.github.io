## Linux相关概念（理解为主）
### Linux版本
redhat
CentOS
Ubuntu
fedora
### Linux特点
开源免费、安全稳定、可移植性好、高性能
### Linux使用领域
应用服务器
数据库服务器
网络服务器
虚拟化云计算
嵌入式
个人pc
移动手机
### Linux主要目录介绍
/：根目录，唯一
/bin：存放命令的目录
/home：用户目录
/root：系统管理员root目录
/usr：应用程序
/etc：系统配置
/boot：内核文件
/tmp：临时文件
### Linux远程连接
查看ip地址 ：**ifconfig**
查看ssh端口（默认22）：**netstat -anpt|grep sshd**
远程连接工具：xshell、finalshell
## Linux命令
### 命令帮助
**-help**（简洁） 例：ls -help
**man** （详细）例：man help
### 查看目录内容（重点）
**ls**
**-l**：以列表形式显示目录或文件的内容
**-a**：显示所有文件或目录，包括隐藏文件
**-h**：显示出文件的目录或大小（单位），必须与l一起使用
ls、
ls -l、ls -a、
ls -lh、ls -la、
ls -lha
ls -lha /usr/bin
### 通配符
通配符可以匹配符合条件的文件或者目录。
＊：表示匹配0到多个任意字符
？：表示匹配单个任意字符
[abcd]:表示匹配括号内(a、b、c、d中的)任意的一个字符
[a-d]:a-d表示的是从a到d的范围，也就是a、b、c、d.从中匹配任意一个字符。
![image](https://github.com/user-attachments/assets/e3635032-8e9c-48bb-9fc7-c269bbd5f0f8)