# Meeting with Ruize-Tang (唐瑞泽)

## 2019-02-26 (周二; 下午)
- ProblemOverflow Q&A site
	- [x] 如何使用编辑器
	- [x] 设置权限（根据分数自动调整）
- 本学期研究计划:
	- **毕业设计:** CAV 实验部分 + 期刊扩展协议验证
		- [ ] 先验证 NICE, Google OT
	- **Jupiter + Refinement 定理证明:** 暂由魏恒峰探索
	- **真实协同编辑系统验证:** 唐瑞泽开始启动探索工作
		- [ ] 三周后, 小组讨论班报告参考文献 PLDI'17: Black-Box-Analysis
	
## 2019-03-08 (周五; 下午)
- 毕业设计兼Jupiter-Refinement研究进展
	- NICE 协议已经写好 (尚未测试)
- ProblemOverflow Q&A site
	- GitHub (code + data + issues)
	- New features: "@", 消息提醒功能, 个人头像、浏览器提示插件、popular tags/tag cloud, 编辑器支持 markdown (+ html)

## 2019-03-15 (周五; 下午)
毕业设计进展:
- [x] 汇报中期答辩报告提纲 (提出修改意见)
- [x] 毕业设计论文提纲

Jupiter-Refinement 研究进展: 
- [x] NICE TLA+ 代码已完成
- [ ] NICE 验证
- [ ] GoogleOT TLA+ 代码及其验证

## 2019-03-22 (周五; 上午)
Jupiter-Refinement 研究进展:
- [x] 讨论了 GoogleJupiter 协议，达成一致理解
- [x] 确定 GoogleJupiter 协议 TLA+ 代码的结构
	- [ ] 引入 ack[r]
	- [ ] 引入 CSend(c) action
- [x] GJupiterImplXJupiter 的大致方向
	- [ ] 一方面, 恢复 XJupier 中的 c2ss 与 s2ss
		- [ ] c2ss 相同; 主要在于 s2ss
	- [ ] 另一方面, 考虑使用 Stuttering 处理多出来的 CSend() action
- 计划:
	- [ ] 在完成 NJupiter, GJupiter, NJupiterImplXJupiter 之后，组织一次 Code Review Meeting
