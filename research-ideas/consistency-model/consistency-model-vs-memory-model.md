# Consistency Models vs. Memory Models

## 说明
- Consistency Model: Distributed Systems (PoEC Framework) 
- Memory Model: Multiprocessor Shared-Memory Systems; Hardware and Programming Languages

个人观点 (有待商榷) 与摘录观点 (难免断章取义)

## 底层系统模型不同:
### 个人观点
- Consistency Model: data replica; 数据有多份副本
- Memory Model: 共享一份数据 (Cache 之类怎么算?)

### 摘录观点
- *"Understanding Eventual Consistency"* @TR13: 殊途同归
> The similarity to C/C++ might come as a surprise. It stems from the fact that modern multiprocessors have a complicated microarchitecture, including a hierarchy of caches with coherence maintained via message-passing——under the hood, a processor is really a distributed system. Optimisations that processors perform produce the same effects as delays and reorderings of messages occurring in a distributed system.

## View 不同
### 个人观点
- Consistency Model: replica's view
- Memory Model: thread's view
### 摘录观点
### TODO
- [ ] Read paper: *"Consistency in Distributed Storage Systems —— An Overview of Models, Metrics, and Measurement Approaches", 2013*

## 考虑的数据对象不同:
### 个人观点
- Consistency Model: Replicated Data Types (需要考虑更丰富的冲突消解策略)
- Memory Model: read/write register (??? Concurrent Data Types 怎么算?)
### 摘录观点
- RDT@POPL14 [PoEC vs. C/C++]:
> We find that, when specialized to last-writer-wins registers, these specifications are very close to fragments of the C/C++ memory model. Thus, our specification framework generalizes axiomatic shared-memory models to replicated stores with nontrivial conflict resolution.
- *"Understanding Eventual Consistency"* @TR13 [Differences]: 
> Our notion of an execution is similar to structures used for defining memory consistency models of hardware and programming languages. In particular, the visibility relaiton is similar to the "reads-from" relation used in such models. Unlike "reads-from", our visibility relation captures all delivered updates, so as to handle replicated data types.

> There exist a number of specifications of shared-memory models weaker than strong consistency, including those combining several consistency levels. All such models assume read-write memory cells, corresponding to our intreg data type. We handle arbitrary replicated data types and, as a consequence, our notion of executions is somewhat different from the one used to define shared-memory models.

> The notion of execution can be simplified in this case: .... Read actions have a single incoming vis edge from the write action it fetches its value from. ...
