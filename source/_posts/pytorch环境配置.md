---
title: anaconda、pytorch、jupyter环境配置
date: 2023-06-30 13:20:03
category: pytorch环境
---

# 下载 anaconda3

anaconda 可以管理 python 环境，通过创建不同的子环境，适应不同的需求，只需要切换到对应的环境中即可。

_创建环境_：`conda  create -n 环境名 python=版本号`  
_激活环境_：`conda activate 环境名`  
_取消激活环境_：`conda deactivate`

官网：<www.anaconda.com>

# 安装 pytorch

_下载安装(cpu 版)_：`pip3 install torch torchvision torchaudio`  
_验证 pytorch 是否安装成功_：进入 python 运行状态，`import torch`  
_验证 gpu_：`torch.cuda.is_available()`

官网：<https://pytorch.org/>

# 安装 jupyter

安装 anaconda 的过程中已经在默认环境中装上了 jupyter 应用程序，现在需要将 jupyter 添加到 pytorch 环境中，激活环境，执行`conda install nb_conda`或者`conda install nb_conda_kernels`，再在该环境中执行`jupyter notebook`启动 jupyter，发现虚拟环境已被添加。
**启动时终端可能会报错，此时需要`pip install web??(忘记是什么包了)`，要安装一个包才行**

## 修改 jupyter 工程目录

统一到一个目录下，<https://blog.csdn.net/weixin_42165744/article/details/127424690>

# import numpy 时可能报错

需要修改 numpy 版本，我改为`pip3 install numpy==1.20.0`即可，(直接安装版本是 1.25.0)
参考博客：<https://blog.csdn.net/one_super_dreamer/article/details/104612443?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-104612443-blog-109199889.235%5Ev38%5Epc_relevant_default_base&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-104612443-blog-109199889.235%5Ev38%5Epc_relevant_default_base&utm_relevant_index=5>

**_python、pytorch、numpy 的版本要对应（版本兼容性很重要）_**
