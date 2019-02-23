# Meeting with Ye-Ji (纪业)

## 2018-10-16 (周二)

两部分工作安排

### Redis: Replicated List 在 Redis 系统中的设计与实现

***项目特色: 基于 Redis、面向 Redis***

- OT 方法
	- [ ] 包括 OT 函数和控制函数 (多向张宇奇和江雪请教)
- CRDT 方法
	- [ ] 先完成 Attiya's RGA 算法的伪代码和TLA验证

### TLA+: State-space Graph 探索
- [ ] 两个工具的探索
- [ ] ***目标***: 交互式的 state-space graph

可能需要学习 Graphviz/Dot 和其它交互式网页设计工具

## 2018-10-29 (周一)
讨论工作进展:
- Redis
	- 初步了解C/S架构
- TLA toolbox (statespace visualizer)
	- 初步了解两个工具

确定近期工作（到本学期末）
- [ ] Redis List 实现
- [ ] TLA toolbox (statespace visualizer)
- [ ] CRDT
	- Attiya's RGA 协议的伪代码与 TLA+ 验证
	- Roh's RGA 协议的伪代码与 TLA+ 验证
	- Attiya's RGA 与 Roh's RGA 的等价性

## 2018-11-06 (周二; 下午)

1. Attiya's RGA 算法的 TLA+ 描述与验证工作:
	- 主要讨论了如何表示Tree结构
		- $G = (V, E)$ 使用node和edge集合表示
		- [ ] 挑战在于: 如何用 TLA+ 描述 tree 上的前序遍历算法
2. 两个 Dot Visualizer 工具
	-	现状: 在简单例子上仍然出错
	-	[ ] 建议: 到 TLA+ Googlegroup 上寻求帮助

## 2018-11-20 (周二; 晚上)

讨论 RGA 协议 (Attiya@PODC2016) 的 TLA+ 描述。讨论了下述内容，也留下了相关的TODO事项:

- [x] 模块化 P2P Comm Module
- [ ] 测试 Tree  的 preorder traversal 操作符

后续可能的新工作:
- [ ] Attya's RGA 与 Roh's RGA 的等价性 (使用 TLA+ 验证)

## 2018-12-04 (周二; 下午)

- 讨论 RGA 协议的 TLA+ 描述
	- 已完成协议描述
	- 已完成 QC 验证
	- [x] 待完成 WLSpec 验证
	- [ ] 待完成 SLSpec 验证
- 讨论研究生阶段工作
	- [x] DynaStore 算法的 TLA+ 描述、验证与定理证明 (暂时弃用该计划)

## 2018-12-07 (周五; 下午)

- 讨论研究生阶段工作 (说明了两个可能的选择)
	- [ ] TLC Debugger (including Animation)
	- [ ] DynaStore 算法的 TLA+ 描述、验证与定理证明
	- [ ] TLA+ + Consistency Model (2018-12-08 添加; 尚未讨论)

## 2018-12-10 (周一; 上午)

- 讨论研究生阶段工作
	- 选择了 TLA+ + Theorem Proving + Consistency Model 工作
	- 推荐了参考资料: 《Principles of Consistency Models》 与 《A Shared Memory Poetics》

## 2018-12-14 (周五; 上午)
- 查看了 TLA+ RGA 的部分代码
- 规划了 TLA+ RGA-tree, RGA-list, Equiv 的论文写作计划
- 规划了 硕士生讨论班 报告计划

## 2018-01-03 (周四; 下午)
- [] 规划硕士生讨论班报告
	- [] 先介绍总体目标
	- [] 再介绍当前完成的工作
- [ ] 规划论文写作
	- [ ] GitHub 私有仓库
	- [ ] 时间表
	- [ ] 现在就开始做 PPT（作为每周的工作进度汇报）

## 2018-01-10 (周四; 下午)
- [x] 硕士生讨论班报告修改建议
