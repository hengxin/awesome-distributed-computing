# Meeting with Xingchen-Yi (易星辰)

## 2018-11-30 (周五; 下午)

讨论 PaxosStore (of WeChat) Refines Voting 的问题:
- [ ] 问题一: Message Exchange in PaxosStore 使得 PaxosStore 中的 ballot、变量可以“大步”变化，这是 Voting 所不允许的。
	- [ ] Message Exchange 属于算法优化，可以先去掉
	- [ ] 添加 Message Exchange 机制，考虑如何使用 Refinement 技术处理它
- [ ] 问题二: All vs. Majority in PaxosStore
	- [ ] 目前认为是 "Majority"
	- [ ] 关于 All 与 Majority 产生不同结果的情况暂时存疑

## 2018-12-04 (周二; 下午; Disalg-Seminar)

易星辰主讲:
- 介绍 PaxosStore@WeChat
- 介绍 Paxos -> Voting -> Consensus 的 Refinement 路线

遇到的问题:

在 PaxosStore 中，由于允许类似 gossip 机制的 acceptor 间信息交换，出现了 Voting 中不允许出现的 maxBallot 与 votes 不同步变化的行为。这使得无法在 PaxosStore 与 Voting 间建立 refinement 关系。

解决方案:
- [ ] 限制 PaxosStore 行为，忽略部分信息
- [ ] 扩展 Voting 行为 (`maxBal' = b` 修改为 `maxBal' >= b`)，包含 PaxosStore 的行为
	- [ ] 扩展后的 Voting 仍然 Refine Consensus

目前倾向于第二种方案。
