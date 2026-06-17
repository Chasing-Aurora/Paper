- **Bootstrap Your Own Latent** - A New Approach to Self-Supervised Learning
- BYOL通过两个神经网络的互相学习，提出了一种==无需负样本的新型自监督图像表示学习方法==，且在多个基准测试中超越了当前的最先进技术

- BYOL依赖于两个神经网络，分别称为在线网络 online network 和目标网络 target network ，它们通过相互作用进行学习。**训练过程首先对同一图像生成两张增强视图，然后 online 网络被训练来预测 target 网络对同一图像增强视图的表示，target 网络通过 online 网络的缓慢移动平均进行更新**。


