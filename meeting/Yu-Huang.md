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
