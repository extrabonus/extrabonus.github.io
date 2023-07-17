# Linux常用命令

以下是一些常用的Linux命令，这些命令可以帮助您进行系统管理、软件安装和配置等任务。以CentOS7为例，同时也包括Ubuntu和SUSE的部分命令。
## 文件和目录管理

```bash
# 列出当前目录下的所有文件和目录
ls

# 切换到指定目录
cd directory_path

# 创建新目录
mkdir directory_name

# 复制文件或目录
cp source_file destination_file

# 移动文件或目录
mv source_file destination_file

# 删除文件
rm file_name

# 删除目录
rm -r directory_name

# 查看文件内容
cat file_name

# 查看文件头部内容
head file_name

# 查看文件尾部内容
tail file_name

# 压缩文件
tar -czvf archive_name.tar.gz file_name

# 解压缩文件
tar -xzvf archive_name.tar.gz
```
## 清除缓存
```bash
# 查看缓存
free -h

# 清除缓存
echo 3 > /proc/sys/vm/drop_caches
echo 1 > /proc/sys/vm/drop_caches
echo 2 > /proc/sys/vm/drop_caches

# 查看进程
ps -ef | grep XXX/java/nginx

# 清理进程
kill -9 PID
```

## 更新和软件包管理

```bash
# 更新软件包列表
sudo yum update

# 安装软件包
sudo yum install package_name

# 升级单个软件包
sudo yum upgrade package_name

# 卸载软件包
sudo yum remove package_name

# 搜索软件包
sudo yum search keyword

# 查看软件包信息
sudo yum info package_name

# 清理不再需要的软件包及其相关依赖
sudo yum autoremove
```

## 系统服务管理

```bash
# 启动服务
sudo systemctl start service_name

# 停止服务
sudo systemctl stop service_name

# 重启服务
sudo systemctl restart service_name

# 关闭开机自启服务
sudo systemctl disable service_name

# 启用开机自启服务
sudo systemctl enable service_name

# 查看服务状态
systemctl status service_name
```
## 防火墙管理

```bash

# 启用或禁用防火墙
sudo systemctl start/stop/restart firewalld

# 显示防火墙状态
sudo firewall-cmd --state

# 显示防火墙端口
sudo firewall-cmd --list-all

# 添加端口
sudo firewall-cmd --zone=<zone> --add-port=<port>/<protocol> --permanent

# 删除端口
sudo firewall-cmd --zone=<zone> --remove-port=<port>/<protocol> --permanent

# 重新加载
sudo firewall-cmd --reload
```
## vim编辑文件

```bash

# 打开文件

vim filename # 打开一个名为filename的文件。

vim # 打开Vim编辑器，可以在其中创建新文件或打开现有文件。

# 退出和保存

:q # 退出Vim编辑器（如果没有进行更改）。

:q! # 强制退出Vim编辑器，放弃所有更改。

:w # 保存文件，但不退出Vim编辑器。

:wq # 保存文件并退出Vim编辑器。

:w filename # 将当前文件保存为filename。

#插入和编辑

按下 i # 进入插入模式，在光标前插入文本。

按下 Esc # 退出插入模式，返回到命令模式。

a # 在光标后插入文本。
o # 在当前行下方插入新行。
O # 在当前行上方插入新行。
r # 替换单个字符。
dd # 删除当前行。
yy # 复制当前行。
p  # 粘贴复制的行或文本。

#移动光标

h # 向左移动一个字符。
j # 向下移动一行。
k # 向上移动一行。
l # 向右移动一个字符。
0 # 移动到行首。
$ # 移动到行尾。
gg # 移动到文件的开头。
G # 移动到文件的结尾。
:n # 跳转到第n行。

#查找和替换

/pattern # 在文件中向下搜索匹配pattern的文本。
?pattern # 在文件中向上搜索匹配pattern的文本。
n  #定位到下一个搜索结果。
N #定位到上一个搜索结果。
:s/pattern/replacement/g # 将当前行中的pattern替换为replacement。
:%s/pattern/replacement/g # 将文件中所有匹配pattern的文本替换为replacement。
```
## 用户和权限管理

```bash
# 创建新用户
sudo adduser username

# 为用户设置密码
sudo passwd username

# 将用户添加到用户组
sudo usermod -aG group_name username

# 删除用户
sudo userdel username

# 修改用户密码
sudo passwd username

# 修改文件或目录的所有者
sudo chown owner_name file_or_directory

# 修改文件或目录的所属组
sudo chgrp group_name file_or_directory

# 修改文件或目录的权限
sudo chmod permissions file_or_directory
```

## Ubuntu常用命令

`apt`：用于管理软件包。通过apt可以安装、更新、卸载软件包，以及查看软件包信息。

```bash
# 更新软件包列表
apt update

# 安装软件包
apt install package_name

# 更新软件包
apt upgrade

# 卸载软件包
apt remove package_name

# 查看软件包信息
apt show package_name
```

`service`：用于管理系统服务。可以启动、停止、重启或重新加载系统服务。

```bash
# 启动服务
service service_name start

# 停止服务
service service_name stop

# 重启服务
service service_name restart

# 重新加载服务
service service_name reload
```

`systemctl`：用于管理systemd服务。可用于启动、停止、重启或重新加载系统服务。

```bash
# 启动服务
systemctl start service_name

# 停止服务
systemctl stop service_name

# 重启服务
systemctl restart service_name

# 重新加载服务
systemctl reload service_name
```

`ufw`：用于管理防火墙规则。可以配置防火墙规则并启用或禁用防火墙。

```bash
# 启用防火墙
ufw enable

# 禁用防火墙
ufw disable

# 允许端口通过防火墙
ufw allow port_number/tcp

# 拒绝端口通过防火墙
ufw deny port_number/tcp
```

## SUSE常用命令

更新和软件包管理

```bash
# 更新软件包列表
sudo zypper refresh

# 安装软件包
sudo zypper install package_name

# 更新软件包
sudo zypper update

# 卸载软件包
sudo zypper remove package_name

# 搜索软件包
sudo zypper search keyword

# 查看软件包信息
sudo zypper info package_name

# 清理不再需要的软件包及其相关依赖
sudo zypper clean
```

