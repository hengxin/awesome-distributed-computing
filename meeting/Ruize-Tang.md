# Meetings

## 2018-10-10 (周三)

主要有两项内容:

### Jupiter Specs 及其实验
现已完成 AJupiter、XJupiter、CJupiter 规约。
接下来需要规划如何做实验。
实验目的包括:
- XJupiter 与 CJupiter 本身的性质
	- [x] $\forall c: sss[c] = css[c]$。
- [x] XJupiter 与 CJupiter 各自满足 SEC 和 WLSpec
-  XJupiter 与 CJupiter 等价
	- [ ] $\bigcup sss \text{ of XJupiter} \equiv css[\text{Server}] \text{ of CJupiter}$
	- [ ] $\forall c \in \text{Client}: css[c] \text{ of XJupiter} \subseteq css[c] \text{ of CJupiter}$

### TLC 外围工具开发
从 TLA Animation 入手。
学习 Video Lecture: [# An Animation Module for TLA+ - William Schultz](https://youtu.be/mLF220fPrP4)，掌握 [Examples](https://github.com/will62794/tlaplus_animation)，在此基础上从事扩展开发。

项目计划：
- [ ] Simulation 模式下支持更丰富、更具可扩展性的 animation (学习 SVG、D3 技术)
- [ ] Model checking 模式下支持交互式的 amimation。
- [ ] 与 real code 联系起来，借助于 animation 做系统测试。

## 2018-10-17 (周三)

### 一周进展如何

### 一周计划

### 毕业设计安排
- 改成: TLA+ Animation (以 Jupiter 为用例)　***[取消]***

## 2018-10-29 (周一 下午)

### 讨论周二小组讨论班的报告
- 梳理逻辑、提纲

### 毕业设计安排

- AbsJupiter
- $\text{XJupiter} \equiv \text{AJupiter}$
  - 定义 Refinement mapping
  - Model checking
  - Manual proof

## 2018-11-01 (周四 晚上)

我介绍了 XJupiterImplCJupiter Module 的关键点:
- XJupiterExtended Module with `soids` and `Cop with sctx`
- $\text{CJ} \triangleq \text{INSTANCE CJupiter WITH} \cdots$
	- $css \gets \cdots$
		- $s2ss$ at the Server
		- $c2ss$ at clients
			- [x] ***遗留问题:*** 这里是重点!!! 有Bug需要调试。
	- $cur \gets \cdots$

## 2018-11-09 (周五 晚上)

### XJupiterImplCJupiter
我介绍 XJupiterImplCJupiter的进展:
- 关键: 去除了CJupiter 中的 soids 以及 Cop 操作的 sctx field; 使用 serial 代替 

### 毕业设计安排
- [ ] AJupiter => XJupiter
- [ ] 阅读 Sun@TPDS09 COT 算法
- [ ] CJupiter => AbsJupiter

### TLA+ 讨论班安排
- [ ] 毕业设计进展/Animation/Prophecy Variables (Cont.)

