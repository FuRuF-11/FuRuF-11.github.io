---
layout: post
title:  "Solomonoff,Kolmogorov and Levin with Compression,Prediction and Search"
date:  2024-01-08
blurb: "所罗门诺夫、柯尔莫哥洛夫和莱文与压缩、预测和搜索"
---
# 所罗门的遗产

将时间调回到1956年的达特茅斯的夏天的末尾，来自于各方的学术巨擘们刚刚结束了为期一个月（会议自8月31日开始）的对于人工智能的讨论，他们当中的大部分都已经离开。

但是，有三个人留了下来（实际上，这三个人一整个夏天都呆在那里进行讨论）。这三个人分别是[马文·明斯基](https://zh.wikipedia.org/wiki/马文·闵斯基)、[约翰·麦卡锡](https://zh.wikipedia.org/wiki/约翰·麦卡锡)还有[雷·所罗门诺夫](https://en.wikipedia.org/wiki/Ray_Solomonoff)。

对于前两者，所有对AI有所学习有所了解的人都不会陌生，但是对于雷·所罗门诺夫（以下简称所罗门），大部分人却闻所未闻。这其实是由于所罗门一生的研究领域，看起来实在是太过抽象、太过偏门且**似乎不像同会议其他人的成果那么有用**。尽管所罗门本人是人类历史上首位使用概率论进行机器学习研究的学者，但是他的主要成就是一门名叫算法概率（Algorithmic probability）——后被发展为算法信息理论（Algorithmic Information Theory）——的古怪学科和关于通用归纳推理的数学理论（General Theory of Inductive Inference）。

但实际上，这位不为人知的雷·所罗门诺夫所提出的理论，正是为如今最伟大的一群AI研究者们（如[Ilya Sutskever](https://en.wikipedia.org/wiki/Ilya_Sutskever)、[Wojciech Zaremba](https://en.wikipedia.org/wiki/Wojciech_Zaremba)、[Marcus Hutter](https://en.wikipedia.org/wiki/Marcus_Hutter)等）指明了研究方向的伟大理论。换句话说，一些世界上最顶尖的头脑真心认为，所罗门的理论，是从数学上可以证明的，**可以被用于实现AGI的理论**。

## AGI的实现理论

我们需要明确的一点是，对于这些人来说，AGI的定义是什么？尽管在学术界并没有确切的、公认的对AGI的定义，但是根据所罗门的理论，我认为可以这样定义AGI：**一种可以对任意给定问题的解自动进行高效搜索的机器**。

首先请让我解释这个定义。对于普罗大众来讲，他们对于AI的期望无外乎一个具有意识的，可以和他们交谈并解答问题，替代他们的日常工作的机器人。我们可以看到GPT就是基本满足了这些需求的一个聊天机器人。人们在使用GPT时往往都是给出问题并希望GPT去回答。这实际上就是利用GPT来自动化的搜索自己提出的问题的解。GPT的回答中的那些客套话和特殊的文法格式，实际上也是在回答OpenAI预设的问题。

即使将现代的AI技术应用在机器人、化学、数学、生物学等各个领域中，我们也实际上是在使用AI在这些领域中去搜索一些特定的问题的解，例如：如何证明拉格朗日定理、蛋白质如何折叠、如何产生新的材料、机器人的位姿动作应该如何调整等等。所以上文中提到的定义实际上是可以涵盖如今我们所有对AGI的期望的。

也许会有人质疑这个定义并没有涉及智能和意识，这似乎与我们期望的真正的人类智能想去甚远。对于这种质疑，我的理论是：人类的智能和意识，是我们的神经系统在亿万年的进化中，就是通过搜索的方式，在求解“活下去”这个问题的过程中，得到的副产物。所以如果我们设置恰当的问题，我们也可以在我提出的这个AGI的定义下得到智能和意识。

接下来需要解释的，就是这个定义中的三个关键词：“自动”，“高效”，“搜索”，在所罗门的理论中是什么样子的。

## 柯尔莫哥洛夫复杂度与压缩

算法概率是所罗门诺夫归纳推理理论的主要成分，它的发明目的是解决一类机器学习问题：给定一系列符号，预测下一个会是哪一个。

在所罗门的算法概率理论，奥卡姆剃刀和多重解释原理占据了相当重要的部分。  
1. 奥卡姆剃刀：如无必要，勿增实体。
2. 伊壁鸠鲁的多重解释原理：如果不止一个理论与观察结果一致，则保留所有此类理论。

## 莱文通用搜索与神经网络

采用所罗门诺夫的理论作为一般性假设的最美妙的地方就在于，他解释了神经网络为何会有如此强的泛化性能。因为按照理论，最小化loss的过程，可以看作搜索柯氏复杂度最小程序的过程，而柯氏复杂度最小的程序是唯一的，且一定是泛化性能最好的。

令人遗憾的是，雷·所罗门诺夫，这位伟大的思想家、AI领域的先驱，已经于2009年永远的离开了我们。但是我可以确定，他深邃而超前的思维将永远伴随着我们，帮助我们捧起AGI的圣杯。R.I.P. 

Referring:  
[所罗门诺夫的个人网站](https://raysolomonoff.com/)   
[所罗门诺夫的归纳推理理论](https://en.wikipedia.org/wiki/Solomonoff%27s_theory_of_inductive_inference)  
[算法概率](https://en.wikipedia.org/wiki/Algorithmic_probability#Overview)  
[柯尔莫哥洛夫复杂度](https://en.wikipedia.org/wiki/Kolmogorov_complexity)  
[译作——老师柯尔莫哥洛夫的生平和工作（9）：1960年代之算法信息论，算法概率论，柯尔莫哥洛夫复杂度（Kolmogorov complexity）](https://zhuanlan.zhihu.com/p/425376986)  
[莱文通用搜索](https://steemit.com/steemstem/@markgritter/leonid-levin-s-universal-algorithm)  
[通用搜索](http://www.scholarpedia.org/article/Universal_search)