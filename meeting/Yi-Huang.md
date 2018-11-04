# Meeting with Yi-Huang （黄弈）

## 2018-10-12 （周五; 晚上）

黄弈介绍了下下周小组讨论的报告提纲。
内容是《Principles of Eventual Consistency》(PoEC, for short) 的前五章。

我们经过讨论，确定了报告重点:
- 要着重讲清楚“History $H$ 满足一致性模型 （即 $\mathcal{C}$” $H \models \mathcal{C}$) 的含义
- 介绍 RDT, 通过示例讲清楚 $\textsf{RVal}$ 的含义
- 介绍该框架下一致性模型的定义方法，介绍常见的一致性模型的定义

我提出的建议:
- 对照阅读 CSUR'16 论文《Consistency in Non-Transactional Distributed Storage Systems》的前两节。找到最合适的讲解逻辑。

未来计划:
- 确立传统的一致性模型框架 (以JACM'14为代表)与新框架 (以PoEC为代表)的等价性
	- 方法一：证明。包括 manual proof 和 coq proof。
	- 方法二：合成。参考论文PLDI'17《Synthesizing Memory Models from Framework Sketches and Litmus Tests》。

## 2018-10-30 (周二; 下午) 

- 经讨论，明确 PLDL'17 论文所关注的是多处理器系统中的内存模型，但是在基本原理上与我们关注的分布式计算中的一致性模型是相同的。对我们来说，PLDL'17 提供了一种研究方法。
- 我推荐了 PLDI'17 论文报告视频

## 2018-11-02 (周五; 晚上)

简单聊了几句。

谈到讨论班报告提纲:
- 总: ***motivation*** (需要着重思考)
- 分: PoEC + MemSynthesis
- 总: 工作计划

提到了 SMT，以后需要重点学习。

