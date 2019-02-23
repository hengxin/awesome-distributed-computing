# Meeting with Yu-Huang (黄宇)

## 2017-10-17 (周三; 下午)

### CCF 稿件
基本定稿，后期做文字修订
- [x] 作者照片

### paper-jupiter Journal 写作
- [x] XJupiter、CJupiter 分别满足 `WLSpec`
- [ ] XJupiter $\equiv$ CJupiter（做法: Model Checking Properties 与证明中用到的定理相对应）

### 唐瑞泽毕业设计安排

仍然做 Jupiter 相关工作（否决了 TLA+ Animation 工作）

需要就此做好规划


## 2018-10-31 (周三; 上午; 电话讨论)

### 关于 "Fast Access to Atomic Memory" 论文的讨论

- Round-based Model 实际上限制了 (server) replica 之间不能通信
- 该文中提出的一轮读算法是有条件的，它限制了读操作的数量
- 多写情况下的弱结论: 不存在“前$k-1$轮读，仅在最后一轮（第$k$轮）写回”的读操作。

### 关于 Refinement 的讨论
确定了两篇需要仔细阅读学习的论文: Lamport关于Byzantine Paxos Refinement的文章以及 TLA+ 代码

DISC11: Byzantine Paxos by Refinement
TR11: The PlusCal Code for Byzantine Paxos by Refinement

## 2018-10-31 (周三; 晚上; 电话讨论)

讨论关于唐瑞泽与马白工作的分配情况:
- 唐瑞泽做 refinement mapping 的 manual proof 与 model checking
- 马白做 refinement mapping 的 theorem proving

## 2018-11-23 (周五; 上午)

暂时放下 PODC'2018 计划:
- [ ] Hamiltonian Path 归约到 IAV 的设想
- 暂时放下

开始 CAV'2018 计划:
- 2月初投稿
- 提上日程
- Jupiter 协议族的 TLA+ 验证 

## 2018-11-29 (周四; 下午)

- [ ] 2018-12-13 分布式算法课程 讲解 Consensus Number
- [x] 安排与易星辰讨论 Paxos Refinement Mapping 的问题
	- [x] 安排在 2018-11-30 (周五; 下午)
- 讨论下步计划 (与唐瑞泽合作)
	- [ ] Plan A: Theorem Proving for Jupiter (当前选定的计划)
	- [ ] Plan B: Synthesis of CMs

## 2018-12-06 (周四; 下午)

1. 讨论易星辰当前关于 Paxos 的工作:
	- 提出新的 Refinement 框架: Paxos -> Voting -> Consensus **+** TPaxos -> Voting' -> Consensus **+** Voting -> Voting'
	- 待研究问题: 在上述 Refinement 框架中, 加入 DSM layer (可能可以参考 Paxos Register 的做法)
2. 讨论纪业后续工作，可能的选择:
	- TLC Debugger (包括但不限于 Animation)
	- TLA+ + DynaStore
	- TLA+ + Consistency Model (2018-12-08 补充)

## 2018-12-07 (周五; 下午)
讨论 TLC 实验的 Distributed Mode:
- [ ] 查看 TLC 帮助文档
- [ ] 在 Docker 中运行多个 TLC 实例 (用于快速测试)

## 2018-12-11 (周二; 上午)
- [ ] 推荐论文《Consensus Refined》，对如何撰写 Refinement 相关的论文有指导作用
- [ ] 推荐论文《Paxos Consensus, Deconstructed and Abstracted》，提到了 Bound-based Register，对处理 Consensus Refinement 中的 DSM Layer 有帮助

## 2018-12-12 (周三; 上午)
- [ ] 讨论 "Coq 小组" 的组建工作
- [ ] 讨论"Unlabeled Transition System" 中的 "Unlabeled" 的含义 (见 Cutoff Bound 论文)
- [ ] Cutoff bound for Jupiter model checking?

## 2018-12-12 (周三; 晚上)
讨论纪业论文写作问题:
- [x] ~~TLA+ for RGA **+** TLA+ for OpSets~~
- [x] TLA+ for RGA-Tree **+** TLA+ for RGA-List **+** Equivalence (采用该方案)
