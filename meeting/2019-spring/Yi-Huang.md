# Meeting with Yi-Huang (黄羿)

## 2019-02-26 (周二; 上午)
1. 讨论两篇论文的阅读情况:
	- CAV'18: Monitoring Weak Consistency
	  - 论文讨论了 Sequential Semantics for RetVal Consistency。
	    是否直接适用于 Concurrent Semantics for RetVal Consistency?
	  - 可 Monitor 的 Consistency Model 有 $vis \subseteq lin$ 以及 $hb \subseteq lin$ 的要求。能否去掉这些约束?
    - POPL'19: VisibilityRelaxation
  	  - 重点关注该文是如何 Relax visibility relation 的以及如何应用到 Java Concurrent Objects。
	  - [ ] 重点阅读该论文, 两周后在小组讨论班上作报告
2. ***Paper:*** Automatically Establishing Equivalence Among Consistency Models Within and Across Axoimatic Frameworks
	- [ ] 完成 Session Guarantees 的形式化描述与等价性证明
	- [ ] Lattice of Session Guarantees (Figure 7 of PLDI'15: DeclarativeProgramming)
3. 博士讨论班时间: 2019-04-?

## 2019-03-07 (周四; 下午)
- VisRelax@POPL'2019 论文讨论:
	- Huang: 介绍了论文主要工作
	- Wei: 讨论三项可能工作:
		- [ ] VisRelax 合成: 自动确认 (而非通过大量人工分析) Visibility Relaxation 的层次
		- [ ] 调研 RDT/CRDT 分布式数据库, 以它们为研究对象重复 VisRelax@POPL'19 工作 (*最近的调研任务*)
		- [ ] 如何量化 visibility/arbitration (参考论文: Quantitative Relaxation of Concurrent Data Structures)
- Equiv 工作进展:
  - [ ] 待完成 Session Guarantees 的形式化描述与等价性证明

## 2019-03-15 (周五; 晚上)
- [ ] 讨论了在 Equiv 工作中遇到的困难: 如何理解 (vis + ar) 框架
- [ ] 确定下下周小组报告: VisRelax@POPL'2019
- [ ] 博士讨论班报告: AutoComp@POPL'2017 (挑战: Data Structures) 

## 2019-03-22 (周五; 晚上)
讨论 VisRelax@POPL'2019 小组报告:
- 还需进一步提炼重点并形成报告提纲
