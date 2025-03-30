---
title: anaconda、pytorch、jupyter环境配置
date: 2023-06-30 13:20:03
category: 机器学习环境
---

# 下载anaconda3  
anaconda可以管理python环境，通过创建不同的子环境，适应不同的需求，只需要切换到对应的环境中即可。

*创建环境*：`conda  create -n 环境名 python=版本号`  
*激活环境*：`conda activate 环境名`  
*取消激活环境*：`conda deactivate`  

官网：<www.anaconda.com>

# 安装pytorch
*下载安装(cpu版)*：`pip3 install torch torchvision torchaudio`  
*验证pytorch是否安装成功*：进入python运行状态，`import torch`  
*验证gpu*：`torch.cuda.is_available()`

官网：<https://pytorch.org/>

# 安装jupyter
安装anaconda的过程中已经在默认环境中装上了jupyter应用程序，现在需要将jupyter添加到pytorch环境中，激活环境，执行`conda install nb_conda`或者`conda install nb_conda_kernels`，再在该环境中执行`jupyter notebook`启动jupyter，发现虚拟环境已被添加。
**启动时终端可能会报错，此时需要`pip install web??(忘记是什么包了)`，要安装一个包才行**

## 修改jupyter工程目录
统一到一个目录下，<https://blog.csdn.net/weixin_42165744/article/details/127424690>

# import numpy时可能报错
需要修改numpy版本，我改为`pip3 install numpy==1.20.0`即可，(直接安装版本是1.25.0)
参考博客：<https://blog.csdn.net/one_super_dreamer/article/details/104612443?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-104612443-blog-109199889.235%5Ev38%5Epc_relevant_default_base&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-104612443-blog-109199889.235%5Ev38%5Epc_relevant_default_base&utm_relevant_index=5>

***python、pytorch、numpy的版本要对应（版本兼容性很重要）***