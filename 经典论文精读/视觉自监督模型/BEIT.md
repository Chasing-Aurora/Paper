
## Pretext
- 在许多无监督学习的研究中，经常提到 **“pretext tasks”**
- **Pretext** 是名词，意思是 **“借口、托词、伪装”**，它通常用于描述一个看似表面上的理由或目的，但实际上它背后可能隐藏着更深层的目的或动机
- **Pretext** = **An excuse or reason given to hide the real purpose**
- 在机器学习和深度学习中，**pretext** 这个词有着稍微不同的含义，它主要指的是为实现某个任务而设计的 辅助任务，这些任务本身并不是最终目标，但它们有助于模型 学习有用的特征
	- ==pretext tasks 辅助任务 不是最终目标任务，但它们帮助模型在没有标签的情况下学习有意义的特征==
- 常见的 Pretext Tasks 示例：
	- **恢复受损的输入数据**：例如**去噪自编码器（Denoising Autoencoders）**，在这种任务中，模型的目标是恢复被噪声破坏的图像或数据。
	- **上下文自编码器（Context Autoencoders）**：学习数据中的上下文信息，帮助模型理解数据的局部结构。
	- **跨通道自编码器（Cross-channel Autoencoders，色彩化）**：例如**图像色彩化**，通过在灰度图像中恢复颜色信息来训练模型。
- 