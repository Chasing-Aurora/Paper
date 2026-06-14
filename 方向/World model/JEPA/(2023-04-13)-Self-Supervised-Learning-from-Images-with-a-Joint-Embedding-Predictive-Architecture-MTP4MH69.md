---
tags: []
parent: 'Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture'
collections:
    - 'World model'
    - JEPA
$version: 1267
$libraryID: 1
$itemKey: MTP4MH69

---
# <span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(238, 249, 253);">(2023-04-13) Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture</span></span>

| <!-- --> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Author:</span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);"> Mahmoud Assran; Quentin Duval; Ishan Misra; Piotr Bojanowski; Pascal Vincent; Michael Rabbat; Yann LeCun; Nicolas Ballas;</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Journal: </span></span><span style="color: rgb(255, 0, 0);"><span style="background-color: rgb(243, 250, 244);">, </span></span><span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">2023.</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Journal Tags:</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Local Link: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);"><a href="zotero://open-pdf/0_2UELNU6U" rel="noopener noreferrer nofollow">Assran 等 - 2023 - Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture.pdf</a></span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">DOI: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);"><a href="https://doi.org/10.48550/arXiv.2301.08243" rel="noopener noreferrer nofollow">10.48550/arXiv.2301.08243</a></span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Abstract: </span></span>***<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">This paper demonstrates an approach for learning highly semantic image representations without relying on hand-crafted data-augmentations. We introduce the Image-based Joint-Embedding Predictive Architecture (I-JEPA), a non-generative approach for self-supervised learning from images. The idea behind I-JEPA is simple: from a single context block, predict the representations of various target blocks in the same image. A core design choice to guide I-JEPA towards producing semantic representations is the masking strategy; specifically, it is crucial to (a) sample target blocks with sufficiently large scale (semantic), and to (b) use a sufficiently informative (spatially distributed) context block. Empirically, when combined with Vision Transformers, we find I-JEPA to be highly scalable. For instance, we train a ViT-Huge/14 on ImageNet using 16 A100 GPUs in under 72 hours to achieve strong downstream performance across a wide range of tasks, from linear classification to object counting and depth prediction.</span></span>* |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Tags:</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Note Date: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">2026/6/8 17:08:34</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |


2h 的讲解视频：<https://youtu.be/t_RvDTzi3vU?t=2>

## <span style="color: rgb(224, 255, 255);"><span style="background-color: rgb(102, 205, 170);">📜 Research Core</span></span>

***

> Tips: What was done, what problem was solved, innovations and shortcomings?

### ⚙️ Content

### 💡 Innovations

### 🧩 Shortcomings

## <span style="color: rgb(32, 178, 170);"><span style="background-color: rgb(175, 238, 238);">🔁 Research Content</span></span>

***

### intro

#### 自监督的方法

*   基于不变性的方法：对同一张图像做裁剪、翻转、色彩变换等数据增广

    *   SimCLR / SimCLRv2：对比学习标杆
    *   MoCo (Momentum Contrast)：动量对比学习，引入**<span style="color: rgb(0, 0, 0);"><span style="">动量编码器 + 队列</span></span>**存储大量负样本
    *   BYOL (Bootstrap Your Own Latent)：依靠**<span style="color: rgb(0, 0, 0);"><span style="">动量网络 + 预测头</span></span>**，仅约束同一图像两个视图特征对齐，彻底摆脱负样本依赖

*   生成式方法：让模型完成图像补全、降噪、重建等生成任务，自主挖掘图像纹理、结构、语义等视觉规律

    *   MAE (Masked Autoencoder)：随机掩码图像大部分区域，模型根据可见像素**<span style="color: rgb(0, 0, 0);"><span style="">还原被遮挡部分</span></span>**
    *   VAE (Variational Autoencoder)：变分自编码器，学习图像隐空间分布，通过**<span style="color: rgb(0, 0, 0);"><span style="">编码 - 解码重建原图</span></span>**实现表征学习
    *   Denoising Autoencoder (DAE)：降噪自编码器，给图像添加高斯噪声、椒盐噪声，模型学习**<span style="color: rgb(0, 0, 0);"><span style="">去噪还原</span></span>**，挖掘底层视觉特征GPT for Vision / iGPT
    *   GPT for Vision / iGPT：将图像像素序列化，用类 Transformer 自回归方式**<span style="color: rgb(0, 0, 0);"><span style="">逐像素生成图像</span></span>**

### 💧 Data

### 👩🏻‍💻 Method

### 🔬 Experiment

### 📜 Conclusion

## <span style="color: rgb(0, 77, 153);"><span style="background-color: rgb(135, 206, 250);">🤔 Personal Summary</span></span>

***

> Tips: What aspects did you question, how do you think it can be improved?

### 🙋‍♀️ Key Records

### 📌 To be resolved

### 💭 Thought Inspiration
