# 1.简介

# 2.下载安装
## 2.1 Anaconda 下载链接
https://repo.anaconda.com/archive/
https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/

## 2.2 安装
```
1.注意选择自定义的安装目录，如果是 windows，尽量不要安装到 c 盘，例如
D:\software\software_for_develop\anaconda
2.勾选的地方
√ Create start menu shortcuts
√ Register Anaconda3 as my default Python 3.11

X 不要勾选 Add Anaconda 3 to my PATH environment variable
3.Install 即可
```

## 2.3 配置环境变量
```
1.找到 Anaconda 安装目录下的 Scripts 目录
D:\software\software_for_develop\anaconda\Scripts
2.将上一步的目录添加到 PATH 中即可
```

## 2.4 验证是否安装成功
```
在菜单栏中打开anaconda命令行，也就是Anaconda Prompt（anaconda3）
点击后，如果能在命令行左侧的括号中看到base，则代表安装成功！

输入 python --version 显示默认python版本
```

## 2.5 配置镜像
```
在用户的家目录(windows：C:\users\username\，linux：/home/username/)生成 .condarc应用程序的配置文件，
此配置文件，是一种可选的（optional）运行期配置文件，其默认情况下是不存在的，
但当用户第一次运行 conda config 命令时，将会在用户的家目录创建该文件。

打开 .condarc 文件添加以下内容

channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/win-64/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/  
  - defaults
show_channel_urls: true
channel_alias: https://mirrors.tuna.tsinghua.edu.cn/anaconda
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```

## 2.6 常用命令
```
1.创建一个名为 chattts, python=3.11 的虚拟环境：
conda create -n chattts python=3.11

2.删除虚拟环境：
conda remove -n chattts --all

3.进入虚拟环境：
activate chattts

4.退出虚拟环境：
deactivate chattts

5.显示全部信息：
conda info

6.显示所有虚拟环境：
conda info --env

7.查看已安装包：
conda list

8.升级包：
pip install --upgrade XXX

9.卸载包：
pip uninstall XXX
```

https://blog.csdn.net/qq_41946216/article/details/129478882 (安装配置 anaconda)

# 2.PyCharm 打开一个项目后，配置过程
```
以 ChatTTS 为例
File -> Settings -> Project: ChatTTS -> Python Interpreter -> 
Add Interpreter -> Add Local Interpreter -> Conda Environment ->
选择本地 Anaconda 的安装目录 Scripts 下的 conda.exe，本文是：
D:\software\software_for_develop\anaconda\Scripts\conda.exe ->
Load Environments -> Create new environment ->
输入 Environment Name 并选择 Python version ->
点击 ok 即可
```
