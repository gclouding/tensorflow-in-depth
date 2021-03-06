# 《深入解析TensorFlow架构设计与实现原理》

### 第一部分 基础篇

# 第1章 TensorFlow系统概述

## 1.1 TensorFlow简介

### 1.1.1 TensorFlow的产生背景

### 1.1.2 TensorFlow的独特价值

### 1.1.3 TensorFlow的版本变迁

### 1.1.4 TensorFlow的目标用户

### 1.1.5 TensorFlow与其他深度学习平台的对比

## 1.2 TensorFlow的设计目标

### 1.2.1 灵活通用的深度学习库

### 1.2.2 端云结合的人工智能引擎

### 1.2.3 高性能的基础平台软件

## 1.3 TensorFlow的基本架构

### 1.3.1 TensorFlow的工作形态

### 1.3.2 TensorFlow的组件结构

## 1.4 小结

# 第2章 TensorFlow环境准备

## 2.1 TensorFlow的安装

### 2.1.1 TensorFlow安装概述

### 2.1.2 使用Anaconda安装

### 2.1.3 使用原生pip安装

### 2.1.4 使用Virtualenv安装

### 2.1.5 使用Docker安装

### 2.1.6 使用源代码编译安装

### 2.1.7 Hello TensorFlow

## 2.2 TensorFlow的依赖项

### 2.2.1 Bazel软件构建工具

### 2.2.2 Protocol Buffers数据结构序列化工具

### 2.2.3 Eigen线性代数计算库

### 2.2.4 CUDA统一计算设备架构

## 2.3 TensorFlow的源代码结构

### 2.3.1 根目录

### 2.3.2 tensorflow目录

### 2.3.3 tensorflow/core目录

### 2.3.4 tensorflow/python目录

### 2.3.5 安装目录

## 2.4 小结

# 第3章 TensorFlow基础概念

## 3.1 TensorFlow编程范式——数据流图

### 3.1.1 声明式编程与命令式编程

### 3.1.2 数据流图在深度学习应用上的优势

### 3.1.3 TensorFlow数据流图的基本概念

## 3.2 TensorFlow数据载体——张量

### 3.2.1 张量——Tensor 

### 3.2.2 稀疏张量——SparseTensor

## 3.3 TensorFlow模型载体——操作

### 3.3.1 计算节点——Operation

### 3.3.2 存储节点——Variable

### 3.3.3 数据节点——Placeholder

## 3.4 TensorFlow运行环境——会话

### 3.4.1 普通会话——Session

### 3.4.2 交互式会话——InteractiveSession

### 3.4.3 扩展阅读：会话实现原理

## 3.5 TensorFlow训练机制——优化器

### 3.5.1 损失函数与优化算法

### 3.5.2 优化器概述

### 3.5.3 简单梯度计算方法

### 3.5.4 扩展阅读：高级梯度计算方法

## 3.6 一元线性回归模型的最佳实践 

## 3.7 小结


### 第二部分 关键模块篇

# 第4章 TensorFlow数据处理方法

## 4.1 输入数据集

### 4.1.1 使用输入流水线并行读取数据

### 4.1.2 创建批样例数据的方法

### 4.1.3 填充数据节点的方法

### 4.1.4 处理CIFAR-10数据集的最佳实践

## 4.2 模型参数

### 4.2.1 模型参数的典型使用流程

### 4.2.2 使用tf.Variable创建、初始化和更新模型参数

### 4.2.3 使用tf.train.Saver保存和恢复模型参数

### 4.2.4 使用变量作用域处理复杂模型

## 4.3 命令行参数

### 4.3.1 使用argparse解析命令行参数

### 4.3.2 使用tf.app.flags解析命令行参数

## 4.4 小结


# 第5章 TensorFlow编程框架

## 5.1 TensorFlow单机程序编程框架

### 5.1.1 单机程序编程框架概述

### 5.1.2 创建单机数据流图

### 5.1.3 创建单机会话

## 5.2 TensorFlow分布式程序编程框架

### 5.2.1 PS-worker架构概述

### 5.2.2 分布式程序编程框架概述

### 5.2.3 创建TensorFlow集群

### 5.2.4 将操作放置到目标设备

### 5.2.5 TensorFlow数据并行模式

### 5.2.6 TensorFlow同步训练机制

### 5.2.7 TensorFlow异步训练机制

### 5.2.8 使用Supervisor管理模型训练

### 5.2.9 Supervisor使用方法进阶

### 5.2.10 扩展阅读：分布式会话创建原理

### 5.2.11 分布式同步训练的最佳实践

## 5.3 小结


# 第6章 TensorBoard可视化工具 

## 6.1 TensorBoard概述

### 6.2.1 TensorBoard典型用例

### 6.2.2 TensorBoard使用流程

## 6.2 可视化数据流图

### 6.2.1 名字作用域与抽象节点

### 6.2.2 可视化数据流图的最佳实践

### 6.2.3 扩展阅读：汇总数据和事件数据

### 6.2.4 扩展阅读：揭秘tf.summary.FileWriter工作原理

## 6.3 可视化学习过程

### 6.3.1 汇总操作概述

### 6.2.2 使用tf.summary.scalar生成折线图

### 6.3.3 使用tf.summary.histogram生成数据分布图

### 6.3.4 使用tf.summary.image生成图像

### 6.3.5 使用tf.summary.audio生成音频

### 6.3.6 可视化MNIST softmax模型学习过程的最佳实践

## 6.4 可视化高维数据

### 6.4.1 使用TensorBoard可视化高维数据

### 6.4.2 可视化MNIST数据集的最佳实践

## 6.5 小结

# 第7章 TensorFlow模型托管工具 

## 7.1 TensorFlow Serving概述

## 7.2 TensorFlow Serving系统架构

## 7.3 TensorFlow Serving的安装

### 7.3.1 使用APT安装ModelServer

### 7.3.2 使用源码编译安装ModelServer

## 7.4 TensorFlow Serving最佳实践

### 7.4.1 导出模型

### 7.4.2 发布模型服务

### 7.4.3 更新线上模型服务

## 7.5 小结

### 第三部分 算法模型篇

# 第8章 深度学习概述

## 8.1 深度学习的发展历史

### 8.1.1 感知机模型与神经网络

### 8.1.2 神经网络的寒冬与复苏

### 8.1.3 神经网络的发展与第二次寒冬

### 8.1.4 深度学习时代的到来 

## 8.2 深度学习的主要应用

### 8.2.1 计算机视觉

### 8.2.2 自然语言处理

### 8.2.3 深度强化学习

## 8.3 深度学习与TensorFlow 

## 8.4 小结

# 第9章 卷积神经网络

## 9.1 CNN模型简介

### 9.1.1 卷积层

### 9.1.2 激活层

### 9.1.3 池化层

### 9.1.4 全连接层

### 9.1.5 Dropout层

### 9.1.6 Batch Normalization (BN)层

### 9.1.7 常用的CNN图像分类模型

## 9.2 TensorFlow-Slim

### 9.2.1 Datasets包和Data包

### 9.2.2 Preprocessing包

### 9.2.3 Deployment包

### 9.2.4 Nets包

### 9.2.5 TensorFlow-Slim最佳实践

## 9.3 CNN模型的应用

### 9.3.1 物体检测

### 9.3.2 图像分割

## 9.4 小结

# 第10章 生成对抗网络

## 10.1 GAN的原理及应用

### 10.1.1 GAN的原理

### 10.1.2 GAN的主要应用

## 10.2 几类经典的GAN模型

### 10.2.1 DCGAN 

### 10.2.2 InfoGAN

### 10.2.3 LPGAN

### 10.2.4 WGAN

### 10.2.5 LS-GAN

## 10.3 GAN模型的发展趋势

## 10.4 小结

# 第11章 循环神经网络

## 11.1 RNN单元及其变种

### 11.1.1 RNN单元

### 11.1.2 LSTM单元

### 11.1.3 GRU单元

### 11.1.4 双向RNN单元

### 11.1.5 带有其他特性的RNN单元

## 11.2 RNN模型

### 11.2.1 PTB-LSTM语言模型

### 11.2.2 Seq2Seq模型

## 11.3 小结

### 第四部分 核心揭秘篇

# 第12章 TensorFlow运行时核心设计与实现

## 12.1 运行时框架概述

## 12.2 关键数据结构

### 12.2.1 张量相关数据结构

### 12.2.2 设备相关数据结构

### 12.2.3 数据流图相关数据结构

## 12.3 公共基础机制

### 12.3.1 内存分配

### 12.3.2 线程管理

### 12.3.3 多语言接口

### 12.3.4 XLA编译技术

### 12.3.5 单元测试框架

## 12.4 外部环境接口

### 12.4.1 加速器硬件接口

### 12.4.2 系统软件接口

## 12.5 小结

# 第13章 通信原理与实现

## 13.1 概述

## 13.2 进程内通信

### 13.2.1 通信接口

### 13.2.2 会合点机制

### 13.2.3 异构设备内存访问

## 13.3 进程间通信

### 13.3.1 gRPC通信机制

### 13.3.2 控制通信

### 13.3.3 数据通信

## 13.4 RDMA通信模块

### 13.4.1 模块结构

### 13.4.2 消息语义

### 13.4.3 通信流程

## 13.5 小结

# 第14章 数据流图计算原理与实现

## 14.1 概述

## 14.2 数据流图创建

### 14.2.1 流程与抽象

### 14.2.2 全图构造

### 14.2.3 子图提取

### 14.2.4 图切分

### 14.2.5 图优化

## 14.3 单机会话运行

### 14.3.1 流程与抽象

### 14.3.2 执行器获取

### 14.3.3 输入数据填充

### 14.3.4 图运行

### 14.3.5 输出数据获取

### 14.3.6 张量保存

## 14.4 分布式会话运行

### 14.4.1 主-从模型

### 14.4.2 主要抽象

### 14.4.3 Client创建会话

### 14.4.4 Client请求图运行

### 14.4.5 Master驱动图运行

### 14.4.6 Worker实施图运行

## 14.5 操作节点执行

### 14.5.1 核函数抽象

### 14.5.2 CPU核函数执行

### 14.5.3 GPU核函数执行

## 14.6 小结

### 第五部分 生态发展篇

# 第15章 TensorFlow生态环境

## 15.1 TensorFlow生态环境概况

### 15.1.1 社区托管组件

### 15.1.2 第三方项目

## 15.2 Keras深度学习算法库

### 15.2.1 Keras 项目概述

### 15.2.2 Keras 模型概述

### 15.2.3 Keras 顺序模型

### 15.2.4 Keras 函数式模型

## 15.3 TensorFlow与Kubernetes生态的结合

## 15.4 TensorFlow与Spark生态的结合

## 15.5 TensorFlow通信优化技术

## 15.6 TPU及神经网络处理器

## 15.7 NNVM模块化深度学习组件

## 15.8 TensorFlow未来发展

## 15.9 小结

#### 附录 A：常见问题解决方案

#### 附录 B：TF社区参与方法与建议

#### 附录 C：勘误方法与作者联系方式

#### 参考资料

