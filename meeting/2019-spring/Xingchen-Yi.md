# Meeting with Xingchen-Yi (易星辰)

## 2019-02-28 (周四; 晚上)
讨论 Paxos Register:
- Consistency Semantics 是 Paxos Register 的语义
- [ ] 仿照 Regular Register (TLA+) 实现 Paxos Register 的语义 (参考 googlegroup)
- [ ] 对于 TPaxos, 可能需要中间层 TPaxos Register。TPaxos Register 是 Paxos Register 的分布式实现 (在 TPaxos 中, 每个 acceptor 保存对其它 acceptors  的 views。)
