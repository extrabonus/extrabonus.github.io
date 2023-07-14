# Linux常用命令

以下是一些常用的Linux命令，这些命令可以帮助您进行系统管理、软件安装和配置等任务。以CentOS7为例。
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

```
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

## 用户和权限管理

```
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

```
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

```
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

```
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

```
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

```
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

