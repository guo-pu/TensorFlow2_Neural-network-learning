# TensorFlow2_Neural-network-learning
综合整理常用的神经网络，包括生物神经网络、人工神经网络、卷积神经网络、循环神经网络、生成对抗网络；文章的结构是先进行概念了解，然后结合图片、结构图、一步一步详细讲解；大家要不看看？然后基于Tensorflow2，和Python3，进行项目实践。

【神经网络】综合篇——人工神经网络、卷积神经网络、循环神经网络、生成对抗网络
--

本文综合整理常用的神经网络，包括生物神经网络、人工神经网络、卷积神经网络、循环神经网络、生成对抗网络；参考了许多高校的课程、论文、博客和视频等。文章的结构是先进行概念了解，然后结合图片、结构图、一步一步详细讲解；大家要不看看？ ( •̀ ω •́ )y

  

一、人工神经网络
--------

**简介：人工神经网络 **(Artificial Neural Network, ANN)，由人工神经元构成的网络，模拟人类的大脑；它模拟生物过程以反映人脑某些特征的计算结构。

**联系**：人工神经元模拟生物神经元；人工神经网络模拟人类的大脑，模拟生物神经网络。

**特点**：人工神经网络是一个并行、分布处理结构，具有学习能力、泛化能力。

**功能**：联想记忆功能、非线性映射功能、分类与识别功能、知识处理功能。

**详细介绍**：**[一篇文章“简单”认识《人工神经网络》(更新版)](https://blog.csdn.net/qq_41204464/article/details/115420602?spm=1001.2014.3001.5501)**

**目录大纲**：

*   1 前言
    
*   2 人类大脑
    
*   3 生物神经网络
    
*   4 生物神经元
    
*   5 人工神经元
    
*   6 人工神经网络
    

*   6.1 单层神经网络
    
*   6.2 多层神经网络
    
*   6.3 前向传播
    
*   6.4 损失函数
    
*   6.5 梯度下降方法
    
*   6.6 反向传播算法
    

*   7 特点
    
*   8 功能
    
*   9 小结
    
*   参考
    

单层神经网络，如下所示图： **( •̀ ω •́ )y**

![](https://img-blog.csdnimg.cn/20210403235150799.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

  

二、卷积神经网络
--------

**简介**

卷积神经网络（Convolutional Neural Network, CNN），通过**卷积层**与**池化层**的叠加实现对输入数据的特征提取，最后连接**全连接层**实现分类。对于图像处理有出色表现，在计算机视觉中得到了广泛的应用。

**联系**

**动物视觉系统**对外界的感知是：

1.  视觉皮层的每个神经元只响应某些特定区域的刺激（感受野）
    
2.  从局部到全局（信息分层处理机制）
    

**卷积神经网络**：

1.  每个神经元只需对 局部图像 进行感知；
    
2.  在更高层将局部的信息综合起来，得到全局信息；
    

**结构**：主要由 卷积层+池化层+全连接层 组成的。

**应用**：图像分类、目标检测、目标跟踪、语义分割、实例分割等。

**详细介绍**：**[一篇文章“简单”认识《卷积神经网络》(更新版)](https://blog.csdn.net/qq_41204464/article/details/115451144?spm=1001.2014.3001.5501)**

**目录大纲**：

*   1 前言
    
*   2 基于什么提出卷积神经网络？
    
*   3 卷积（Convolution）
    
*       3.1 卷积操作
    
*       3.2 多层卷积层
    
*   4 池化（Pooling）
    
*   5 全连接层
    
*   6 特征维度变化
    
*   7 CNN核心思想——参数共享
    
*   8 优势
    
*   9 经典的卷积神经网络
    
*   10 卷积神经网络应用
    
*   参考
    

基本卷积神经网络，如下所示图： **( •̀ ω •́ )y**

![](https://img-blog.csdnimg.cn/20210406014623697.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

  

三、循环神经网络
--------

**简介**：**循环神经网络**（Recurrent Neural Networks，RNN），是一种反馈网络，模拟“人脑记忆功能”，常用于语言识别、机器翻译、视频分析、生成图像描述等。

**背景**：人工神经网络、卷积神经网络是前馈网络；前馈神经网络是一个静态网络，信息的传递是单向的，网络的输出只依赖于当前的输入，不具备记忆能力。前馈神经网络处理的数据是一个一个输入的，前后数据没有关系的。实际生活中，很多数据都是有上下文相关性的，这些数据称为序列数据；处理的时候，不能只考虑当前的输入就进行判断，需要考虑前后之间关系。

这时需要使用“循环神经网络”，它能有效处理**序列特性**的数据，它能挖掘数据中的**时序信息**以及**语义信息**。

**结构**：循环神经网络由循环体堆叠而成；

**详细介绍：[一篇文章“简单”认识《循环神经网络》(更新版)](https://blog.csdn.net/qq_41204464/article/details/115532353?spm=1001.2014.3001.5501)**

**应用**：主要在**自然语言处理**方向应用；

*   文档分类和时间序列分析（识别文章的主题）
    
*   时间序列对比　　（比较两个文档的相关程度）
    
*   序列到序列的学习（中文翻译为英文）
    
*   情感分析　　　　（推文或电影评论的情感划分为正面或负面）
    
*   世间序列预测　　（根据最近的天气数据来预测未来天气）
    

**目录大纲**：

*   1 前言
    
*   2 循环体
    
*   3 循环神经网络
    
*   4 LSTM网络
    
*   5 循环神经网络应用
    
*   参考
    

循环体及其**按时间展开**后的效果： **( •̀ ω •́ )y**

![](https://img-blog.csdnimg.cn/2021041716470311.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

  

四、生成对抗网络
--------

**简介**：**生成对抗网络**（GAN，generative adversarial network），是一种常用于**学习类别特征**的神经网络结构；主要有两部分组成，分别是生成网络、判别网络。

**背景**：在监督学习中，训练集需要大量的人工标注数据，并且需要人工判断生成结构好坏，这个过程是高成本且低效率的；**GAN**能自动完成这个过程，效率高成本低。

**详细介绍：[一篇文章“简单”认识《生成对抗网络》(GAN)](https://guo-pu.blog.csdn.net/article/details/115611150)**

**应用**：GAN 的应用十分广泛，它的应用包括图像合成、图像编辑、风格迁移、图像超分辨率以及图像转换，数据增强等。

**目录大纲**：

*   1 前言
    
*   2 生成对抗网络应用
    
*      2.1 风格迁移
    
*      2.2 图像生成
    
*      2.3 音乐创作
    
*   3 生成学习算法
    
*   4 生成对抗网络
    
*      4.1 GAN的简要实现流程
    
*      4.2 GAN算法实现要点
    
*   5 MNIST 案例
    
*   6 GAN优点
    
*   7 GAN缺点
    
*   8 文献学习
    
*   1\. Generative Adversarial Networks  
    2\. Conditional GANs  
    3\. DCGAN  
    4\. Improved Techniques for Training GANs  
    5\. Pix2Pix  
    6\. CycleGAN  
    7\. Progressively Growing of GANs  
    8\. BigGAN  
    9.NAS
    

生成对抗网络GAN原理图，如下图所示：**( •̀ ω •́ )y**

![](https://img-blog.csdnimg.cn/20210412082017907.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

  

**大家加油呀~~ ****( •̀ ω •́ )✧**


【神经网络-入门实践】综合篇——物体识别、花朵分类、猫狗识别、风格迁移、文本分类
--

本文综合整理神经网络的入门实践，包括物体识别、花朵分类、猫狗识别、风格迁移、文本分类；参考了官网和许多高校的课程、论文等。文章的结构是一步一步详细讲解，并动手实践；大家要不看看？ ( •̀ ω •́ )y

  

开发环境
----

> Tensorflow2、Python3

  

一、物体识别
------

**简介**

本文介绍卷积神经网络的入门案例，通过搭建和训练一个模型，来对10种常见的物体进行识别分类；使用到CIFAR10数据集，它包含10 类，即：“飞机”，“汽车”，“鸟”，“猫”，“鹿”， “狗”，“青蛙”，“马”，“船”，“卡车” ；共 60000 张彩色图片；通过搭建和训练卷积神经网络模型，对图像进行分类，能识别出图像是“汽车”，或“鸟”，还是其它。

**思路流程**

1.  导入 CIFAR10 数据集
    
2.  探索集数据，并进行数据预处理
    
3.  构建模型（搭建神经网络结构、编译模型）
    
4.  训练模型（把数据输入模型、评估准确性、作出预测、验证预测）  
    
5.  使用训练好的模型
    

**数据集效果图**

![](https://img-blog.csdnimg.cn/20210505160602714.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

**网络结构**

![](https://img-blog.csdnimg.cn/20210505162735254.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

详细介绍：[手把手搭建一个【卷积神经网络】](https://blog.csdn.net/qq_41204464/article/details/116381750?spm=1001.2014.3001.5501)

  

二、花朵分类
------

**简介**

本文介绍卷积神经网络的入门案例，通过搭建和训练一个模型，来对几种常见的花朵进行识别分类；

使用到TF的花朵数据集，它包含5类，即：“雏菊”，“蒲公英”，“玫瑰”，“向日葵”，“郁金香”；共 3670 张彩色图片；通过搭建和训练卷积神经网络模型，对图像进行分类，能识别出图像是“蒲公英”，或“玫瑰”，还是其它。  
![](https://img-blog.csdnimg.cn/20210509174519555.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

**意义**

本篇文章主要的意义是带大家熟悉卷积神经网络的开发流程，包括数据集处理、搭建模型、训练模型、使用模型等；**更重要的是解在训练模型时遇到“过拟合”，如何解决这个问题，从而得到“泛化”更好的模型。**

**思路流程**

1.  导入数据集
    
2.  探索集数据，并进行数据预处理
    
3.  构建模型（搭建神经网络结构、编译模型）
    
4.  训练模型（把数据输入模型、评估准确性、作出预测、验证预测）  
    
5.  使用训练好的模型
    
6.  优化模型、重新构建模型、训练模型、使用模型
    

**模型效果**

在训练和验证集上查看损失值和准确性：

![](https://img-blog.csdnimg.cn/2021050920520383.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

详细介绍：[“花朵分类“ 手把手搭建【卷积神经网络】](https://blog.csdn.net/qq_41204464/article/details/116567051?spm=1001.2014.3001.5501)

  

三、猫狗识别
------

**简介**

本章带大家熟悉“迁移学习”的开发流程，介绍如何使用预先训练好的神经网络，结合实际的功能需求，来实现一些图像任务；比如：实现对猫和狗的图像进行分类。

预先训练好的神经网络，通常称为“预训练模型”，它在大型数据集上进行训练，取得业界认可的效果，开源给广大开发者使用的模型。本文主要介绍在keras中的关于图像任务的开源模型。

**迁移学习方式**

我们可以直接使用预训练模型，毕竟效果挺好的；提供输入信息，经过模型处理，直接输出结果。

也可以使用预训练模型的一部分网络结构，使用其特定的功能（比如：特征提取），然后根据给定任务自定义搭建一部分网络结构（比如：实现分类），最后组合起来就形成一个完整的神经网络啦。本文主要将这种方式。

**思路流程**

1.  导入数据集
    
2.  探索集数据，并进行数据预处理
    
3.  构建模型（搭建神经网络结构、编译模型）预训练模型 \+ 自定义模型
    
4.  训练模型（把数据输入模型、评估准确性、作出预测、验证预测）  
    
5.  使用训练好的模型
    

**模型效果**

![](https://img-blog.csdnimg.cn/20210513011525161.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

详细介绍：[迁移学习之快速搭建【卷积神经网络】](https://mp.csdn.net/editor/html/116720400)

  

四、风格迁移
------

**简介**

风格迁移，基于A图像内容，参考B图像的风格（名画，像毕加索或梵高一样绘画），创造出一幅新图像。

**原理**

风格迁移是基于生成对抗网络实现的，是一种优化技术，用于将两个图像，A图像内容和B图像风格，混合再一起，是输出的图像看起来像A图像，但是也参考了B图像的风格。

通过优化输出图像，以匹配A图像的内容统计数和B图像的风格统计数据。这些统计数据可以使用卷积网络从图像中提取。

**项目实践**

本文基于TF-Hub开源项目进行开发，60多行代码快速实现神经网络的风格迁移，为方便大家使用，已经整理相关代码和模型到[Github](https://github.com/guo-pu/Tensorflow2)中，直接下载即可使用。

**模型效果**

![](https://img-blog.csdnimg.cn/20210519232725273.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

详细介绍：[神经网络之风格迁移【TF-Hub开源项目】](https://blog.csdn.net/qq_41204464/article/details/117048238?spm=1001.2014.3001.5501)

  

五、文本分类
------

**简介**

本文介绍神经网络的案例，通过搭建和训练一个模型，来对电影评论进行“文本分类”；将影评分为_积极_或_消极_两类；是一个二分类问题。

使用到网络电影数据库的 IMDB 数据集，包含 50,000 条影评文本，这是二元情绪分类的数据集。

**意义**

本篇文章主要的意义是带大家熟悉神经网络的开发流程，包括数据集处理、搭建模型、训练模型、使用模型等；**更重要的认识“迁移学习”的开发流程，使用业界认可的网络模型作为“预训练模型”，提高开发效率。**

**思路流程**

1.  导入数据集
    
2.  探索集数据，并进行数据预处理
    
3.  构建模型（搭建神经网络、编译模型）
    
4.  训练模型（把数据输入模型、评估准确性、作出预测、验证预测）  
    
5.  使用训练好的模型
    
6.  优化模型、重新构建模型、训练模型、使用模型
    

**设计模型**

![](https://img-blog.csdnimg.cn/20210524221129277.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

**模型结构**

![](https://img-blog.csdnimg.cn/20210520224825823.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxMjA0NDY0,size_16,color_FFFFFF,t_70)

详细介绍：[【迁移学习】快速实现“文本分类“](https://blog.csdn.net/qq_41204464/article/details/117092259?spm=1001.2014.3001.5501)

  

**小彩蛋**

**[【神经网络】综合篇——人工神经网络、卷积神经网络、循环神经网络、生成对抗网络](https://blog.csdn.net/qq_41204464/article/details/115797030?spm=1001.2014.3001.5501)**

  

**大家加油呀~~ ****( •̀ ω •́ )✧**
