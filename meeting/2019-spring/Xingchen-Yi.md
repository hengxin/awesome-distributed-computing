# Meeting with Xingchen-Yi (易星辰)

## 2019-02-28 (周四; 晚上)
讨论 Paxos Register:
- Consistency Semantics 是 Paxos Register 的语义
- [ ] 仿照 Regular Register (TLA+) 实现 Paxos Register 的语义 (参考 googlegroup)
- [ ] 对于 TPaxos, 可能需要中间层 TPaxos Register。TPaxos Register 是 Paxos Register 的分布式实现 (在 TPaxos 中, 每个 acceptor 保存对其它 acceptors  的 views。)

## 2019-03-18 (周一; 下午)
讨论 Paxos Register 的 TLA+ 实现:
- [ ] Regular Register 的 TLA+ 实现 (如何表示“并发”?)
- [ ] Paxos Register 先初步达成一个理解, 发邮件向作者咨询
	- [ ] 主题: 如何判定给定 execution 满足 Paxos Register 规约
	- [ ] 问题: 如何区分 total vs. partial writes
	- [ ] 我们目前的理解方式
	- [ ] BTW: 不明确的定义
