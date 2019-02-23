# Meeting with Ruize-Tang (唐瑞泽)

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
	- [x] $\bigcup sss \text{ of XJupiter} \equiv css[\text{Server}] \text{ of CJupiter}$
	- [x] $\forall c \in \text{Client}: css[c] \text{ of XJupiter} \subseteq css[c] \text{ of CJupiter}$

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
- [x] AJupiter => XJupiter
- [ ] 阅读 Sun@TPDS09 COT 算法
- [x] CJupiter => AbsJupiter

### TLA+ 讨论班安排
- [ ] 毕业设计进展/Animation/Prophecy Variables (Cont.)

## 2018-11-20 (周二; 下午)

讨论本科毕业设计开题报告

确定了报告题目和报告提纲，基本不需要大的改动

- [x] 2018-11-26 (下周一) 发给我，再作最后的调整

## 2018-12-05 (周三; 上午)
- [ ] AJupiter 的 #states 与 #distinct states 与 XJupiter/CJupiter 不同。这可能意味着错误或者未发现的 AJupiter 与众不同的地方
	- [ ] 通过两个具体的测试用例定位可能的TLA+描述错误
- 保持关注 Symmetry Set (包括 tlaplus-googlegroup 中的问题)
	- [ ] ***将 Client 与 Priority 绑定:*** Client 定义为自然数，用作 Priority
- [x] TLAPS
	- [x] Chapter 10 & Chapter 11 of Hyperbook (已分配: 唐瑞泽)
	- [x] Paper: TLA+ Proofs (已分配: 易星辰)
- [ ] JMX profiling
	- [ ] Disk IO
	- [ ] Hotspot Methods

## 2018-12-13 (周四; 下午)
1. "Jupiter-Project":
   - [x] `Do(c)` 如何放到 Jupiter Interface 的层面上? 尤其是如何将 Operation Generation 相关的逻辑分离出来?
2. JupiterRefinment 论文写作
   - [x] 抽取 Hyperbook 中有关 TLA+ 代码展示的 Commands

## 2018-12-25 (周二; 上午)
- [x] TLAPS Report 修改建议

## 2018-12-27 (周四; 下午)
- [x] 整理Hyperbook TLA+ 代码生成命令
- [ ] 学习 TikZ, 绘制 Jupiter protocol 示意图

## 2019-01-03 (周四; 下午)
1. Jupiter-Project:
	- [ ] AJupiter: # of states testing (high priority)
	- [ ] History variable (low priority)

## 2019-01-14 (周一; 上午)
1. Jupiter-Project:
	- [ ] 统计 Lamport/TLA+ Examples/Resources 实验规模 (两周时间)
	- [ ] 学习 COT 算法，重点关注 COT Conditions 与 SEC/WLSpec 的关系。
		- [ ] 本科毕业设计先证明 AbsJupiter 相关定理（然后是 CJupiter REFINE AbsJupiter 的相关定理）
	- [ ] 检查 paper-jupiter-refinement 草稿

## 2019-01-17 (周四; 上午)
- [ ] Jupiter-Project:
	- [ ] 实验: Model Checking Results
	- [ ] tla2tex 脚本 (建立 GitHub 仓库)
		- [ ] detect all modified tla files
		- [ ] .new => .tex
		- [ ] cp to destination folder
		- [ ] delete  (keep the comment lines)
		- [ ] args: -s (src folder); -d (dest folder); -v (vertical space; using ratio); -font
		- [ ] framed code for formatting
		- [ ] keywords color

## 2019-01-23 (周三; 上午)
- [ ] 建立 GitHub 仓库, 注意收集“研究想法”
- [x] 推荐论文: PLDI'17: Systematic Black-Box Analysis of Collaborative Web Applications
	- [ ] 可能的研究问题 TLC guided testing; Testing open-source collaborative text editing systems
- [x] 推荐论文: FM'14: "Formal Verification of Operational Transformation"
- [x] 提及AJupiter 状态数问题: 易星辰遇到类似问题

## 2019-
- [ ] Cutoff bounds for Jupiter & COT
- [ ] QA 系统
- [ ] TLC Trace Explorer
