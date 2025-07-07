---
title: 用conda创建python虚拟环境
date: 2018/10/21
last_modified_at: 2018/10/22
tags: 命令 Python
categories: 随记
---

1.  conda常用的命令

```zsh
conda -V # 查看版本

conda list # 查看安装了哪些包。

conda env list 或 conda info -e # 查看当前存在哪些虚拟环境

conda update conda # 检查更新当前conda
```

2.  创建python虚拟环境。

```zsh
 # 命令创建python版本为X.X、名字为your_env_name的虚拟环境。your_env_name文件可以在Anaconda安装目录envs文件下找到。
 conda create -n your_env_name python=X.X（2.7、3.6等)
```

3.  使用激活(或切换不同python版本)的虚拟环境。

```zsh
#打开命令行输入python --version可以检查当前python的版本。

#使用如下命令即可 激活你的虚拟环境(即将python的版本改变)。
# Linux:  
source activate your_env_name(虚拟环境名称)

# Windows: 
activate your_env_name(虚拟环境名称)
```

   这是再使用python --version可以检查当前python版本是否为想要的。

4.  对虚拟环境中安装额外的包。

```bash
# package到your_env_name中
conda install -n your_env_name [package]
```

5.  关闭虚拟环境(即从当前环境退出返回使用PATH环境中的默认python版本)。

```zsh
   # Linux: 
   source deactivate
   # Windows: 
   deactivate
```

6.  删除虚拟环境

```zsh
conda remove -n your_env_name(虚拟环境名称) --all
```

7.  删除环境中的某个包

```zsh
conda remove --name your_env_name  package_name
```

