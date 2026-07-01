---
tags: []
parent: 'EchoJEPA: A Latent Predictive Foundation Model for Echocardiography'
collections:
    - 'World model'
    - JEPA
$version: 3320
$libraryID: 1
$itemKey: S9PUK8DP

---
# <span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(238, 249, 253);">(2026-02-02) EchoJEPA: A Latent Predictive Foundation Model for Echocardiography</span></span>

| <!-- --> |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Author:</span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);"> Alif Munim; Adibvafa Fallahpour; Teodora Szasz; Ahmadreza Attarpour; River Jiang; Brana Sooriyakanthan; Maala Sooriyakanthan; Heather Whitney; Jeremy Slivnick; Barry Rubin; et al.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Journal: </span></span><span style="color: rgb(255, 0, 0);"><span style="background-color: rgb(243, 250, 244);">, </span></span><span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">2026.</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Journal Tags:</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Local Link: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);"><a href="zotero://open-pdf/0_84QQEUT2" rel="noopener noreferrer nofollow">Munim 等 - 2026 - EchoJEPA A Latent Predictive Foundation Model for Echocardiography.pdf</a></span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">URL: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);"><a href="https://arxiv.org/abs/2602.02603v4" rel="noopener noreferrer nofollow">https://arxiv.org/abs/2602.02603v4</a></span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Abstract: </span></span>***<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Foundation models for echocardiography often struggle to disentangle anatomical signal from the stochastic speckle and acquisition artifacts inherent to ultrasound. We present EchoJEPA, a foundation model trained on 18 million echocardiograms across 300K patients, representing the largest pretraining corpus for this modality to date. By leveraging a latent predictive objective, EchoJEPA learns robust anatomical }representations that ignore speckle noise. We validate this using a novel multi-view probing framework with frozen backbones, where EchoJEPA outperforms leading baselines by approximately 20% in left ventricular ejection fraction (LVEF) estimation and 17% in right ventricular systolic pressure (RVSP) estimation. The model also exhibits remarkable sample efficiency, reaching 79% view classification accuracy with only 1% of labeled data versus 42% for the best baseline trained on 100%. Crucially, EchoJEPA demonstrates superior generalization, degrading by only 2% under physics-informed acoustic perturbations compared to 17% for competitors. Most remarkably, its zero-shot performance on pediatric patients surpasses fully fine-tuned baselines, establishing latent prediction as a superior paradigm for robust, generalizable medical AI.</span></span>* |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(219, 238, 221);">Tags:</span></span>**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">Note Date: </span></span>**<span style="color: rgb(25, 60, 71);"><span style="background-color: rgb(243, 250, 244);">2026/6/24 22:33:56</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |


# <span style="color: rgb(224, 255, 255);"><span style="background-color: rgb(102, 205, 170);">📜 Research Core</span></span>

***

> Tips: What was done, what problem was solved, innovations and shortcomings?

## 单词的学习

*   readily：<span style="color: rgba(13, 13, 13, 0.9);"><span style="background-color: rgb(255, 255, 255);">乐意地</span></span>

<!---->

*   echo cardio graphy：<span style="color: rgba(0, 0, 0, 0.95);">心脏回声成像，标准译名</span>**<span style="color: rgba(0, 0, 0, 0.95);">超声心动图（心脏彩超）</span>**

    *   <span style="color: rgba(0, 0, 0, 0.95);">echo-：回声；cardio-：心脏；-graphy：成像 / 检查技术</span>
    *   <span style="background-color: rgba(255, 212, 0, 0.5);">cardiac </span><span style="color: rgba(0, 0, 0, 0.95);"><span style="background-color: rgba(255, 212, 0, 0.5);">/ˈkɑːdiæk/</span></span><span style="background-color: rgba(255, 212, 0, 0.5);">：</span><span style="color: rgba(0, 0, 0, 0.95);"><span style="background-color: rgba(255, 212, 0, 0.5);">心脏的；与心脏相关的</span></span>

*   disentangle：<span style="color: rgba(0, 0, 0, 0.95);">dis-（分开、解除）+ entangle（纠缠、缠绕）→ 解开缠绕；理清混杂事物</span>

*   anatomical <span style="color: rgba(0, 0, 0, 0.95);">/ˌænəˈtɒmɪkl/</span>：<span style="color: rgba(0, 0, 0, 0.95);">anatomy（解剖学）+ 形容词后缀 -ical</span>

*   stochastic /stəˈkæstɪk/  ： 随机的——————<span style="color: rgba(0, 0, 0, 0.95);">deterministic  确定性的</span>

*   speckle <span style="color: rgba(0, 0, 0, 0.95);">/ˈspekl/  ：名词斑点，动词 布满斑点</span>

*   <span style="background-color: rgba(255, 212, 0, 0.5);">acquisition artifacts ：</span>**<span style="color: rgba(0, 0, 0, 0.95);"><span style="background-color: rgba(255, 212, 0, 0.5);">采集伪影</span></span>**<span style="color: rgba(0, 0, 0, 0.95);"><span style="background-color: rgba(255, 212, 0, 0.5);">，多见于影像科学（CT/MRI/ 显微成像）、信号采集、传感器领域</span></span>

*   corpus <span style="color: rgba(0, 0, 0, 0.95);"> /ˈkɔːpəs/ </span>：<span style="color: rgba(0, 0, 0, 0.95);">指大量真实文本、语音素材的集合</span>

*   acoustic perturbations

    *   acoustic <span style="color: rgba(0, 0, 0, 0.95);">/əˈkuːstɪk/ ：acoustic wave 声波</span>

    *   <span style="color: rgba(0, 0, 0, 0.95);">perturbations /ˌpɜːtəˈbeɪʃnz/ ：mental perturbations 心绪纷乱</span>

*   pedi atric <span style="color: rgba(0, 0, 0, 0.95);">/ˌpiːdiˈætrɪk/ </span>：<span style="color: rgba(0, 0, 0, 0.95);">pediatric department 儿科</span>

*   paradigm <span style="color: rgba(0, 0, 0, 0.95);">/ˈpærədaɪm/</span>：scientific paradigm 科学范式

*   conscious control：<span style="color: rgba(0, 0, 0, 0.95);">有意识调控 / 主观自主控制</span>

    *   <span style="color: rgba(0, 0, 0, 0.95);">指人凭借清醒主观意识主动管控自身行为、情绪、思维、动作，而非本能、潜意识自动驱动</span>

*   real world implications：<span style="color: rgba(0, 0, 0, 0.95);">实际的现实意义</span>

    *   not just like funny toy problems

*   kidney：<span style="color: rgba(0, 0, 0, 0.95);">肾脏</span>

*   urine：<span style="color: rgba(0, 0, 0, 0.95);">尿，尿液</span>

    *   <span style="color: rgba(0, 0, 0, 0.95);">urine test 尿检</span>

*   morovix paradox：<https://youtu.be/GLeC88evwgk>

    *   paradox /ˈpærədɒks/：悖论；自相矛盾的人 / 事

*   redact /rɪ'dækt/：vt. 编辑,编写，<span style="color: rgb(0, 0, 0);"><span style="background-color: rgb(255, 255, 255);"> </span></span>**<span style="color: rgb(0, 0, 0);"><span style="background-color: rgb(255, 255, 255);">删除、隐藏私人或敏感信息</span></span>**

    *   *<span style="color: rgb(0, 0, 0);"><span style="background-color: rgb(255, 255, 255);">redacted document</span></span>*<span style="color: rgb(0, 0, 0);"><span style="background-color: rgb(255, 255, 255);">（已编辑或隐藏敏感信息的文档）</span></span>

    *   <span style="background-color: rgba(255, 212, 0, 0.5);">在法律、政府或保险文件中，公开前常会对敏感信息进行 redaction 处理</span>

## ⚙️ Content

### 引入

语言非常擅长描述事物，但是 不是真实的感觉 到运动的规律

#### The slowness of Being

*   The slowness of Being

    *   海量输入，贫瘠输出
    *   词不达意是天生不可避免的
    *   <span style="background-color: rgba(255, 102, 102, 0.5);">文字、语言是极度压缩、失真的工具，是低分辨率、低代表性的表示方法</span>
    *   <span style="background-color: rgba(255, 102, 102, 0.5);">language is a much lower bandwidth information</span>
    *   <span style="background-color: rgba(255, 102, 102, 0.5);">describe the world rather than understand the world</span>

> <span style="color: rgb(0, 0, 0);">Our senses take in an enormous, high-dimensional stream (~10⁹ bits/s), but our conscious control and behavior appear limited to ~10 bits/second.</span>
>
> <span style="color: rgb(0, 0, 0);">我们感官每秒摄入海量、高维度信息流（约 10 亿比特），但我们能有意识掌控、向外输出的行为，带宽仅每秒 10 比特。</span>

> <span style="color: rgb(0, 0, 0);">Because what comes out (words/actions) is so bandwidth-limited relative to what goes in, language is an poor proxy for understanding.</span>
>
> **<span style="color: rgb(0, 0, 0);">因为输出（语言、行动）相比输入带宽极度匮乏，语言根本无法完整还原我们内心真实的理解与感受。</span>**

#### Sensory Data

*   Sensory Data（感官数据）

    *   <span style="background-color: rgba(255, 212, 0, 0.5);">视觉感官</span>**<span style="background-color: rgba(255, 212, 0, 0.5);">信息密度</span>**<span style="background-color: rgba(255, 212, 0, 0.5);">远高于文字，文字是高度压缩、抽象的信息；而视觉是高维度、高密度原始感官数据。</span>

    *   短短几年的视觉观察，信息量就能匹敌人类全部互联网文字积累。

*   <span style="background-color: rgba(255, 212, 0, 0.5);">LLM 更多是 </span>**<span style="background-color: rgba(255, 212, 0, 0.5);">pattern match </span>**<span style="background-color: rgba(255, 212, 0, 0.5);">模式匹配，本质就是一个概率模型，可能会出现幻觉，对于 未见过的数据很难应对</span>

    *   LLM  很难做一个 完全智能的，自己能够 盈利的智能体！！！

#### morovix paradox

*   morovix paradox 这种悖论实际上正是人工智能下一阶段发展方向转变的核心原因

    *   from  purely cognitive models like llms  toward embodied、 multimodal、 physical ai systems
    *   <span style="background-color: rgba(255, 212, 0, 0.5);">the next phase of ai development will involve physical ai and world models</span>
    *   ![\<img alt="" width="483" height="278" data-attachment-key="UNPX5LT9" src="attachments/UNPX5LT9.png" ztype="zimage"> | 483](attachments/UNPX5LT9.png)

> <span style="color: rgb(0, 0, 0);">"It is comparatively easy to make computers exhibit adult level performance on intelligence tests or playing checkers, and difficult or impossible to give them the skills of a one-year-old when it comes to perception and mobility."</span>
>
> <span style="color: rgb(0, 0, 0);">翻译：</span>
>
> <span style="color: rgb(0, 0, 0);">让计算机在智力测试、下跳棋这类任务上达到成年人水平相对容易；但在感知、肢体行动这类能力上，赋予它一岁婴儿都具备的技能，却极其困难，甚至几乎做不到。</span>

## 💡 Innovations

## 🧩 Shortcomings

# <span style="color: rgb(32, 178, 170);"><span style="background-color: rgb(175, 238, 238);">🔁 Research Content</span></span>

***

## 💧 Data

## 👩🏻‍💻 Method

## 🔬 Experiment

## 📜 Conclusion

# <span style="color: rgb(0, 77, 153);"><span style="background-color: rgb(135, 206, 250);">🤔 Personal Summary</span></span>

***

> Tips: What aspects did you question, how do you think it can be improved?

## 🙋‍♀️ Key Records

## 📌 To be resolved

## 💭 Thought Inspiration

*   所以 JEPA 非常适合 的就是 医学影像领域！！！

    *   EchoJEPA！！！

        *   可以用于 其他的 疾病/其他的超声 迁移过来！！！
        *   \==把最新 的通用JEPA 的方法迁移过来！！！==

    *   因为 很多医学影响 已经包含了 大量噪声和伪影

    *   <span style="background-color: rgba(255, 212, 0, 0.5);">JEPA 用于医学分割（加权的Multi-block），还有 JEPA用于 影像重建</span>

        *   单独训练 解码器 重新回到像素空间哦，<span class="highlight" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F19634653%2Fitems%2FJQFXTF5V%22%2C%22pageLabel%22%3A%229%22%2C%22position%22%3A%7B%22pageIndex%22%3A8%2C%22rects%22%3A%5B%5B420.54974164679976%2C244.91535000000002%2C555.3060461487999%2C254.87795%5D%2C%5B315.213%2C232.96035%2C555.3040286483993%2C242.92295%5D%2C%5B315.213%2C221.00535000000002%2C556.9705723763991%2C230.96795%5D%2C%5B315.213%2C209.05035%2C437.16640203719953%2C219.01295%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F19634653%2Fitems%2F8MBK8GEP%22%5D%2C%22locator%22%3A%229%22%7D%7D" ztype="zhighlight"><a href="zotero://open/library/items/JQFXTF5V?page=9">“we use the V-JEPA pretrained models to predict the representations of the missing regions, and then use the decoder to project the representations to pixel space.”</a></span><span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F19634653%2Fitems%2F8MBK8GEP%22%5D%2C%22locator%22%3A%229%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/8MBK8GEP">Bardes 等, 2024, p. 9</a></span>)</span>

<!---->

*   MC-JEPA：引入动态理解 用于 实时的分割

*   LeWordModel——端到端 低参数，去分割 超低参数实时部署的，结合其他wm 的关键提点的方法

    *   比如 深度监督！
    *   比如 结合MC-JEPA！！！
    *   提高 长程规划的能力

<!---->

*   有点像 对比学习 的两个网络相互学习：

    *   经过2018年以来视觉领域对比学习的蓬勃发展，其基本的训练框架基本统一，并且有用的tricks也被互相借鉴和验证
    *   所以 看看相关工作的 innovation

*   <span style="background-color: rgba(255, 212, 0, 0.5);">分层 JEPA（H-JEPA, Hierarchical JEPA），每一层就可以看作 传统网络的一层，利用Resnet等的技巧！残差连接+注意力机制！</span>

    *   <span style="background-color: rgba(255, 212, 0, 0.5);">尺度、多粒度的多模态建模，可以利用mdfformer 的深层监督哦</span>

<!---->

*   \~\~多模态的JEPA：结合sam 的输入语言和 图片，能够进一步 提高分割的效果！
*   在 **流形（Manifold）** 中进行了推演，把握了“彻底放弃像素重建、直接在抽象空间中推演环境演变”的核心
*
