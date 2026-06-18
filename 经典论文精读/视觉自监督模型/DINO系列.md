- DINO 是视觉 Transformer 做自监督学习的非常经典的工作
- ==DINO是自监督学习与ViT结合的开创性工作==


# 动机
- 正值Vision Transformer (ViT)大火，其证明了Transformer也可以用于视觉任务，并且在ImageNet取得了SOTA的结果。但ViT尚未展现出相对CNN显著的优势：**ViT对算力要求更高，需要更多的训练数据**，结果看也仅CNN高一点点，并且其训练得到的特征本身并不具备独特的性质
- 作者想探究一下使用自监督学习(Self-supervised Learning)，而不是监督学习(Supervised Learning)的方式，是否会让Vision Transformer性能更好。其**动机来源于Transformer 在 NLP 领域取得成功的主要因素之一是使用了自监督预训练**，例如BERT 的 Masked Language Modeling 或者 GPT 的 Language Modeling
- 然而，在图像领域，==图像级别的监督训练任务通常会将图像中包含的丰富视觉信息简化，从而导致学习到的特征不够优质==

# DINO v1
## 方法
![](../../imgs/2026-06-18/file-2026-06-18-160007668.png)


- 一张图片 x 的两个 View x1,x2 分别输入给学生模型 $g_{θs}$ 和教师模型 $g_{θt}$。两个网络具有相同的架构但参数不同。教师网络的输出通过一个 Batch 的平均值进行 centering 操作，每个网络输出一个 K 维的特征，并使用 Softmax 进行归一化。然后使用交叉熵损失作为目标函数计算学生模型和教师模型之间的相似度。
- ==在教师模型上使用停止梯度 (stop-gradient, sg) 算子来阻断梯度的传播，**只把梯度传给学生模型**使其更新参数。教师模型**使用学生模型的 EMA 进行更新**==





# DINO V2



- scaling up是AI领域常见的发展策略，类似NLP中GPT系列通**过增大模型和数据规模实现能力跃升**，视觉领域通过这种方式能让模型学习到更通用、更精细的视觉特征