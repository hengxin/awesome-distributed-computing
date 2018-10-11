# Meetings

## 2018-10-10 周三

主要有两项内容:

### Jupiter Specs 及其实验
现已完成 AJupiter、XJupiter、CJupiter 规约。
接下来需要规划如何做实验。
实验目的包括:
- XJupiter 与 CJupiter 本身的性质
	- [ ] 在 final state, $\forall c: sss[c] = css[c]$。
- XJupiter 与 CJupiter 各自满足 SEC 和 WLSpec
-  XJupiter 与 CJupiter 等价
	- [ ] $\bigcup sss \text{ of XJupiter} \equiv css[\text{Server}] \text{ of CJupiter}$
	- [ ] $\forall c \in \text{Client}: css[c] \text{ of XJupiter} \subseteq css[c] \text{ of CJupiter}$
### TLC 外围工具开发
从 TLA Animation 入手。
学习 Video Lecture: [# An Animation Module for TLA+ - William Schultz](https://youtu.be/mLF220fPrP4)，掌握 [Examples](https://github.com/will62794/tlaplus_animation)，在此基础上从事扩展开发。
计划：
- [ ] Simulation 模式下支持更丰富、更具可扩展性的 animation (学习 SVG、D3 技术)
- [ ] Model checking 模式下支持交互式的 amimation。
- [ ] 与 real code 联系起来，借助于 animation 做系统测试。
