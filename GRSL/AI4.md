[toc]
## 提交
>我正在完成多模态遥感语义分割的论文，这篇论文是关于接受RGB和DSM多模态的数据然后进行融合，之后进行语义分割后输出。现在正在看method 部分，希望你可以帮助我。创新：具体计了CSFM模块和SDEM模块，通过shuffle,exchange and extract不同模态的信息，从而促进更高效的多模态互补信息的挖掘和融合。还有中间用于加工处理的两个模块会接受到深度监督信号从而在提高训练效率同时增强对于多尺度特征学习的能力。 之后我会传给你图片，然后需要你按照一般论文的形式介绍流程，等到具体创新部分时候，需要给出latex形式公式放到论文上去。明白了吗？

首先给你一张总体结构的图，这个对应论文中的Overall Framework部分
![输入图片说明](/imgs/2025-02-06/uQsOm3HYKEbYSEco.png)
其工作流程：
提出的MDFformer可以接受这两个模态的输入( )，以多尺度的方式高效融合跨模态信息。MDFformer 使用在ImageNet-1k数据集上进行预训练的Mix Transformer encoder (MiT-B1)作为backbone.

At first,a dual-stream encoder 分别提取来自两个输入的数据源的特征by通过4个连续的**TransformerBlock.**同时，在每一个Block之后会通过分支进入CSFM中，用于shuffle and interact多尺度特征，之后它的输出除了返回到主干分支上还会通过一个SDEM 模块进一步增强特征。最后多个SDEM的多尺度特征的输出are fed into FPN head decoder.Notably,FPN所融合的不同尺度的特征图在前向推理的期间会产生自己额外的损失，而在反向传播的过程中会收到来自总损失和自身损失的两个梯度流。这样类似深度监督的方法可以进一步保证中间层多尺度特征的有效训练。As a result,MDFformer可以进行多尺度特征的一系列处理，以层次化的方式融合了浅层和深层的信息。


简单介绍输入图片的维度，这个用行内公式描述，融到一句话里面

你差不多明白这个MDFformer的工作原理了吗？我检验一下你的理解程度

对的，理解正确了。接下来是具体的模块了，需要有计算公式体现呢，但是基本按照下边的步骤进行： 1. 上边先说这个模块的流程 2. 这个什么什么功能的计算可以被描述为：如下的数学公式 3. where定义里面的变量 4. 简单总结一下 总共除去内容中的公式的话，大约300个单词哦 明白了吗？首先我会传给你CSFM模块的设计图和我给你的一些提示，你需要结合之前的总体设计理解一下他这样设计的原理，写在模块处理流程里面 对于公式的话你就看图说话，如果你仔细看深度学习很多文章的公式，基本上都是Y=f(X)的形式的，也就是说告诉读者输入（X）是啥，用什么（f(·)）处理的，输出（Y）是啥而已。不用害怕，明白我的意思了吗？




**Potsdam****数据集**:分辨率--6000*6000px --24patches

Multispectral channels---R-G-B-IR channels and DSM data extracted from Lidar

For training---2_10, 2_12, 3_11, 3_12, 4_11, 4_12, 5_10, 5_12, 6_7, 6_8, 6_9, 6_10, 6_12,7_7, 7_8, 7_9, 7_10, 7_11

For testing---2_11, 3_10, 4_10, 5_11, 6_11, 7_12

**Vaihingen****数据集:**分辨率--6000*6000px True Orthophotos---24patches  

Multispectral channels---R-G-B-IR channels as well as normalized DSM

For training--- 1, 3, 7, 11, 13, 17, 23, 26, 28, 32, 34, 37

For testing--- 5, 15, 21, 30

**Classes**--- roads, buildings, low vegetation(low veg.), trees, cars and clutter

## 返修

<!--stackedit_data:
eyJoaXN0b3J5IjpbODcxMjcwNTNdfQ==
-->