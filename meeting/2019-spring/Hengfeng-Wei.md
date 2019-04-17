# Meeting with Hengfeng Wei (Myself)

## 2018-11-01 (周四)
- [ ] 思考为何需要提出基于 Visibility Relation 的一致性模型框架
  - [ ] 更 general? (Gotsman@POPL'14)
- [ ] 思考黄弈讨论班报告（PoEC + MemSynthesis）提纲 

## 2019-02-03 (周日)

CRDT + Minimal Coordination

CRDT => The Strongest: Causal+ (Attiya:PODC15)
Sync cannot be eliminated

## 2019-02-26 (周二)
***Paper Equiv@2019:*** Automatically Establishing Equivalence Among Consistency Models Within and Across Axoimatic Frameworks
- [ ] 论文具体任务:
  - [ ] 完成 Session Guarantees 的形式化描述与等价性证明 (***DDL: 2019-03-17*** )
  - [ ] 完成 PRAM & Causal 的形式化描述与等价性证明 (***DDL: 2019-03-24***)
  - [ ] Lattice of Session Guarantees (Figure 7 of PLDI'15: DeclarativeProgramming)
- [ ] 学习任务:
	- [ ] MemSAT
	- [ ] Kodkod
	- [ ] MemSynth (PLDI'17:MemSynth)
	- [ ] diy: test-generation tool (CAV'10: Fences in weak memory models) 

## 2019-03-10 (周日)
***Paper Equiv@2019:***
- VisRelax@POPL'2019 中的 Java 测试可以用于***合成***一致性模型（能够满足所有测试的最弱的一致性模型; 能否进一步量化? 量化合成?）

***DCM:***
- Session Guarantees:
	- Combine session guarantee (in Bayou) and quorum (in Cassandra)
	- Defined on each individual operations (mixed consistency)

## 2019-03-14 (周四)
Paper MemSynth@PLDI'2017:
- TSO: $ppo_{\text{TSO}} \triangleq po - (\text{Write} \to \text{Read})$; TSO 不要求 read 看到 (vis relation) 前面的 writes

Paper DisjointSet:
- Learning OT Functions???

## 2019-03-20 (周三)
关于 $(vis, ar)$ 框架:
- 要不要在 relation 中添加类似 $W \times R$ 的限制? 有何影响?
	- 比如 RMW: $so \subseteq vis$ 还是 $so|_{W \times R} \subseteq vis$?
- 要不要分别考虑 per-object 与 cross-object
- 为什么不要求 $read\text{-}from \subseteq vis$?
- 是否假设 $vis \subseteq ar$?
- 是否假设 $hb \subseteq ar$? (Timed Consistency Models)
- $\text{Ret}$ 使用 sequential specification 还是 concurrent specification，有何影响?	
- $read\text{-}from$ 关系与“是否允许写重复值”
- 使用 $(vis, ar)$ 框架表达 PRAM 遇到 "$ar$ 是否是全局统一"的困难
	- [x] 同样的问题是否出现在 CausalConsistency 中? (是的)
	- [x] 在 cs-theory 上[提问](https://cstheory.stackexchange.com/q/42556/12739)
	- [x] 邮件 to Gotsman
		- [ ] 两种可能的修复方法
			- [ ] fix the definition for CC: 修改 $vis$ for CC
			- [ ] allow different $ar$s for different sessions or even operations

## 2019-03-21 (周四)
阅读论文 RelaxVisibility@POPL'2019:
- [ ] ***考察 Redis/Riak 是否有同样的问题?***
- [ ] "monotonic visibility" 与 "peer visibility" 有种对偶 (对称) 的感觉
	- [ ] 分别对应于 "monotonic reads" 与 "monotonic writes"。
	- [ ] 如果将它们放在一起，是什么?
- [ ] 使用 "hbs" 刻画同步原语
- [ ] 形式化框架
	- program $p = \langle po, hbs \rangle$, 其中 $hbs$ 刻画所有可能的同步顺序。要求: $po \subseteq hbs$。
	- behavior $b = \langle hb, ret \rangle$ 刻画一次执行的结果。在给定的执行中, $hb$是确定的, $ret$ 是每个操作的返回值
	- linearization $l = \langle lin, vis \rangle$。$lin$ 是全序, $hb \subseteq lin$。

思考 GoogleJupiter 协议 (ConvOT@CSCW'2014):
- 协议中需要注意的地方:
	- Local Processing: Stop and Wait
	- Server Processing: Buffer 中已有操作不被转换
	- Remote Processing: 与 Jupiter 协议相同
- 正确性:
	- Client: 
	- Server:
- GJupiter 在 Refine 图中的位置:
	- Client: 
	- Server:
- 借鉴 GJupiter 协议:
	- [ ] 能否设计Server与Client都仅需维护一个 Buffer 的 Jupiter 协议?

## 2019-03-22 (周五)
Paper VerifyCC@:
- Verifying causal consistency: ***cutoff bounds***
- Section 3.1:
  > In general, specifications can be defined as sets of posets instead of sequences. This is to model conflict-resolution policies which are more general than choosing a total order between operations.
  - 根据该点, 有可能可以 FIX $(vis, ar)$ 框架在 CC/PRAM 中的 $ar$ 问题。

- Section 4.4: 本文中的 CM (Causal Memory) 是通常理解的 causal consistency。CC 弱于 CM。CCv 强于 CM。CCv 与 CM 不可比。
- Section 4.5: CCv (Causal Convergence) 对应于 Burckhardt 中的 causal consistency。
- 受到很大启发:
	- 需要阅读的相关文献: 
	- [ ] ***Idea:*** Verifying Strong Eventual Consistency of Optimistic Replication Systems (可能会有 cutoff bounds 结果)

## 2019-03-23 (周六)
阅读论文 VerifyEC@POPL'2014:
- Introduction
	- 将 Eventual Consistency 分成 Safety 与 Liveness 两部分，值得借鉴
	- Safety 部分使用 partial order。这与 $(vis, ar)$ 框架中的 $vis$ 相似。
	- ***Liveness 部分也使用 partial order***。这是与 $(vis, ar)$ 框架中的 $ar$ 不同的地方，值得借鉴

## 2019-03-25 (周一)
阅读论文 VerifyEC@POPL'2014:
- ORS: replica-centric, 不是 session-centric
- Local interpretation $li[o]$ 不考虑操作的返回值
	- 可以用 $vis$ relation 表示
- Global interpretation $gi[o]$ 建模 liveness
	- 对实现有影响 (否则会有 trivial 的实现满足 safety)
	- 但是在规约层面重要吗?
	- 还有其它有意义的 liveness condition 吗?

扩展 $(vis, ar)$ 框架:
- 两部分: local part + global part
- local part 是 per-session view, 沿用 $vis$
	- 如何解释这个 $vis$ 由具体数据类型决定 $\mathcal{F}$
- global part 约束 all-session view (比如 $ar$ 所发挥的作用), 沿用 $ar$, 但是使用 partial order

## 2019-03-26 (周二)
- [x] 完成 cav2019-rebuttal 初稿 (与Ruizhe-Tang 讨论)
	- [ ] Jupiter Figures (Tang) 
- [x] 参加小组讨论班 (Yi-Huang: VisRelax@POPL'2019)

## 2019-03-27 (周三)
- [ ] 提交 cav2019-rebuttal
- [ ] 计划投稿 FM'2019
	- [ ] FM'2019 Abstract Registration
- [x] 完成 android + fm 报告并发送给曹老师
