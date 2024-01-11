---
layout: post
title:  "Kolmogorov and Solomonoff and Compress and Prediction"
date:  2024-01-08
blurb: "柯罗格廖夫与所罗门诺夫与压缩与预测"
---
# 所罗门的遗产

将时间调回到1956年的达特茅斯的夏天的末尾，来自于各方的学术巨擘们刚刚结束了为期一个月（会议自8月31日开始）的对于人工智能的讨论，他们当中的大部分都已经离开。

但是，有三个人留了下来（实际上，这三个人一整个夏天都呆在那里进行讨论）。这三个人分别是[马文·明斯基](https://zh.wikipedia.org/wiki/马文·闵斯基)、[约翰·麦卡锡](https://zh.wikipedia.org/wiki/约翰·麦卡锡)还有[雷·所罗门诺夫](https://en.wikipedia.org/wiki/Ray_Solomonoff)。

对于前两者，所有对AI有所学习有所了解的人都不会陌生，但是对于雷·所罗门诺夫（以下简称所罗门），大部分人却闻所未闻。这其实是由于所罗门一生的研究领域，看起来实在是太过抽象、太过偏门且**似乎不像同会议其他人的成果那么有用**。尽管所罗门本人是人类历史上首位使用概率论进行机器学习研究的学者，但是他的主要成就是一门名叫算法概率（Algorithmic probability）——后被发展为算法信息理论（Algorithmic Information Theory）——的古怪学科和关于一般化归纳推理的理论（General Theory of Inductive Inference）。

但实际上，这位不为人知的雷·所罗门诺夫所提出的算法概率理论，正是为如今最伟大的一群AI研究者们（如[Ilya Sutskever](https://en.wikipedia.org/wiki/Ilya_Sutskever)、[Wojciech Zaremba](https://en.wikipedia.org/wiki/Wojciech_Zaremba)、[Marcus Hutter](https://en.wikipedia.org/wiki/Marcus_Hutter)等）指明了研究方向的伟大理论。换句话说，一些世界上最顶尖的脑袋真心认为，所罗门的理论，是从数学上可以证明的，**可以被用于实现AGI的理论**。

## AGI理论

首先，我们需要明确的一点是，对于这些人来说，AGI的定义是什么？尽管在学术界并没有确切的、公认的对AGI的定义，但是根据所罗门的理论，我认为可以这样定义AGI：**一种可以对任意给定问题的解进行高效的自动搜索的机器**。

从这个定义来讲，GPT类的语言模型不是AGI（尽管他确实可以进行高效的自动搜索），它们仅仅是可以自动的搜索一部分问题的解

## 柯罗格廖夫的压缩

算法概率是所罗门诺夫归纳推理理论的主要成分，它的发明目的是解决一类机器学习问题：给定一系列符号，预测下一个会是哪一个。

在所罗门的算法概率理论，奥卡姆剃刀和多重解释原理占据了相当重要的部分。  
1. 奥卡姆剃刀：如无必要，勿增实体。
2. 伊壁鸠鲁的多重解释原理：如果不止一个理论与观察结果一致，则保留所有此类理论。

## 所罗门搜索与莱文通用搜索

Referring:  
[所罗门诺夫的个人网站](https://raysolomonoff.com/)，令人遗憾的是，这位伟大的思想家、AI领域的先驱，已经于2009年永远的离开了我们。AGI的名字中一定会有你的部分，RIP。