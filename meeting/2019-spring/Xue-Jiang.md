# Meeting with Xue-Jiang (江雪)

## 2019-03-07 (周四; 下午)
- Disjoint Set 工作
	- [x] 新的“Split"操作语义满足 EC 的算法以及正确性证明 (下周)
- Memory Synthesis 工作
	- [ ] 近期重点: 重现 MemSynth 工作
		- [ ] 论文: MemSynth@PLDI'2017
		- [ ] 论文: Rosette@Onward'2013
		- [ ] 论文: AutoComp@POPL'2017
	- [ ] 博士生讨论班安排 (希望在重现 MemSynth 工作的基础上能将其部分应用到分布式一致性模型下)

## 2019-03-14 (周四; 下午)
- Disjoint Set 工作
	- [x] 讲解了Split新的语义(语义二)下的算法 (应该是正确的)
	- [ ] 论文安排
		- [ ] Split 语义一(SoftSplit)下满足 EC 的 OT 函数设计
		- [ ] Split 语义二(HardSplit)下满足 EC 的 OT 函数设计
		- [ ] Split 语义二下满足 ECC 的 OT 函数设计
		- [ ] 继续探索新的 Split 语义与应用场景 (MIT Thesis)
		- [ ] Commutative 相关论文 (待整理)
			- [ ] Learning Commutativity Specifications
			- [ ] Learning OT Functions???
		- [ ] OT Control Algorithm 不再重要
		- [ ] TLA: 验证 OT 函数与 OT 算法
		- [ ] 实验

论文 MemSynth@PLDI'2017:
	- 解释部分符号用法
	- 暂时作为博士讨论班内容
		- [x] 下周二: 报告提纲

## 2019-03-21 (周四; 下午)
Disjoint Set 工作:
- 场景 motivation 不足，严重影响论文进展
- 可能会搁置该计划

MemSynth@PLDI'2017:
- 讨论报告提纲:
	- 以 MemSynth 为主, Verification 等为次
	- 报告时要有实验演示
	- 学习顺序: Ocelot => Rosette => MemSynth => Racket
