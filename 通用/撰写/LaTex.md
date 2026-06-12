> [参考文章，推荐](https://blog.csdn.net/ayaishere_/article/details/123332393)
> LaTeX论文 分为 序言、正文两个部分：
>> - 序言部分：主要负责申明论文文体、导入宏包（部分功能的实现需要导入其他的插件协助完成，将这些套件称为“宏包”）、表明文章的标题、作者及时间等信息
>>- 正文部分：主要负责论文的主体内容书写
>
>
>LaTeX中，几乎所有命令都需要依赖于“ \”符，`\命令名称{}`

# 编辑器
## [overleaf——ORCID登录的](https://cn.overleaf.com/project)
-  优点
	1. 云端同步，所有的文件都存储在服务器上，不用担心文件丢失
	2. 大家都是使用**同一套编译和编辑环境**，有什么问题可以很快找到解决方案
	3. 支持**文件历史记录**，对于版本迭代十分友好
	4. 支持多人协作
	5. 随时随地有个浏览器就可以开始写作
- 缺点
	1. 不支持多屏，无法将预览界面放到其他显示器上。目前有一个折中的方案，可以将两个显示器设为拼贴模式，然后调整编辑区和预览区，使预览区正好在第二个显示器上。但是我现在是笔记本带一个显示器，无法设置拼贴！并且Overleaf的预览区也不支持双页视图，即使拖到一个显示器上，效果也不怎么好。
	2. 参考文献数据库bib无法引用本地的文件，对于用JabRef管理参考文献的人不太友好。
	3. 对于使用 `\include{}` 和 `\input{}` 分割内容的文档，在编辑区无法识别目录，但是感觉无伤大雅，因为一般大家都是在预览区通过反向搜索快速跳转的

### [reCAPTCHA报错](https://zhuanlan.zhihu.com/p/428218814)·
- 验证码被blocked的问题，把梯子改成全局模式就好了
- 把一些可能会拦截/检测请求的插件，全禁用一下，就能正常登录了；登录了再恢复。  可能引起问题的的插件：Adblock、Wappalyzer、Evernote Web Clipper、Axure RP Extension、Country Flags & IP Whois、Proxy SwitchyOmega、Switch UserAgents、EditThisCookie等等等等



## 电子邮件和从属关系
- 添加学校 邮箱  以访问您的大学或机构的任何升级，使合作者更容易找到您！！！



## [latex.ustc](https://latex.ustc.edu.cn)
- 




## [本地跑latex](https://www.jianshu.com/p/3a6f1acf794f)
###  VS Code + TeX Live
[vscode+latex+copilot !!!](https://www.bilibili.com/video/BV1HSZWBJEoT/?vd_source=2ea943732094f768d31ea553f4cad800)
[科研技巧 | VS Code 本地部署 LaTeX：环境配置教程](https://mp.weixin.qq.com/s/E_YpykhGIQobRbP4d5JP2Q?poc_token=HPSvF2qjTJ_3AUOIDmfslDSC3LdkkQIdkIlc1OjJ)

- 本地环境还有一个非常重要的优势：**可以更方便地结合 AI 工具提升写作效率**



- 优点
	1. VS Code **界面十分好看，用来写作对眼睛很友好**
	2. 使用 SumatraPDF 进行预览，完美支持双屏显示器
- 缺点
	1. 配置很麻烦，小白直接劝退，后期遇到问题的可能性有比较高

### TeXstudio + TeX Live + SumatraPDF 编辑
- 是比较传统的一种方式
- 优点
	1. TeXstudio 提供了很多快捷操作以及 Latex 命令的提示，比如希腊字母，常用操作符的命令提示
	2. 对于从 CTex 套装过来的人们更亲切一点，操作界面很相似
- 缺点
	1. **白色页面**对眼睛太不友好了，没有提供一个比较好的暗色主题
	2. 需要配置编译器以及默认的构建命令，对于小白有点难度

###  CTex 套装
-  优点
	1. 易上手，全程傻瓜式安装，无需考虑任何配置
	2. 模板巨多，基本从师兄师姐手里传下来的都是支持 CTex 套装的模板
- 缺点
	1. 默认使用`GB 2312`进行编码，而其余三种方式都是主流的`UTF-8`，导致很多人用其他编辑器打开在 CTex 套装中使用过的文件时显示乱码，直接劝退一大波小白使用新的方式进行 Latex 写作
	2. 安装时会删除系统环境变量中`Path`的全部内容，对其他软件例如Java，Matlab会产生严重干扰
	3. 实现中文写作的方式过于古老，编译速度较慢



# 序言
- 序言部分即代码段 **\begin{document} 前**（红色框）的内容。Overleaf 系统已经生成了默认代码，我们可以对其进行微调
- 通过安装**宏包**可以扩展或提供更多的功能。多数情况下，我们简称宏包为“**包**”
- 当你需要完成某项功能时（如导入图片），直接在搜索引擎上搜索相关宏包的代码即可
```
\documentclass[字号,纸张类型]{文本类型}
\usepackage[可选选项]{包名}
\usepackage{times}   % 设置字体为Times New Roman
\usepackage{mathptmx}  % 同时设置文本和数学字体为 Times 风格，实现全文统一
\usepackage{graphicx}  % 使用graphicx包添加图片
\usepackage{amsmath}   % 每次写论文在序言部分不分青红皂白地导入数学包，可以帮助你省很多事

\graphicspath{ {images/} }  % 设置图片的路径

\title{标题名称}
\author{作者}
\date{日期}


\setlength{\parindent}{2em}           %段首缩进两字符，em就是element，par就是paragraph
\setlength{\parskip}{1em}   % 段落间会自动产生与文档字体同高的空行


```
# 正文
- 正文部分即代码段 **\begin{document} 到** **\end{document}** （蓝色框）的内容
- 其实如果不讲究所谓格式与排版，我们可以在**document环境**中编辑任意内容，与正常的Word输入没有两样。凡是在document环境中的内容，都是论文的正文
- “**环境**”，即使用\begin{ }**和**\end{ }**两个命令包裹代码块，使**文本内容具有特殊格式**或**对内容进行标识
- LaTeX通常将论文分为三个层级，通常是**部分、子部分、子子部分**。对应的命令为： **\section**{}、**\subsection**{}、**\subsubsection**{}，括号内为该部分的名称
- 在LaTeX中**单个“Enter”键并没有真正的换行效果**，需要使用命令操作
- 对于有序列表，我们使用**enumerate**环境；对于无序列表，我们需要使用**itemize**环境。但无论哪种类型，每个条目前面必须有控件序列 **\item**，作为条目标识符
- [LaTeX 数学公式与希腊字母 参考](https://blog.csdn.net/qq_41775769/article/details/121362953)
```
\begin{document}

\maketitle   % 序言部分设置的标题、作者、日期得以显示
\section{Introduction}
\includegraphics{tupian}

$E=mc^2$  % 内联模式，我们有许多方法可以表示，我推荐使用一对美元符号 包裹目标公式
\[ E=mc^2 \]  % 无编号的显示模式，我推荐使用 “ \[ ” 和 “ \] ”包裹目标公式
\begin{equation}
E=m
\end{equation}   % 有编号的显示模式，我推荐使用equation环境包裹

\end{document}
```


