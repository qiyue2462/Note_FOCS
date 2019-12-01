# 第十章 软件工程

本章主要讨论软件工程的相关基础知识

## 软件生命周期

软件生命周期指的是软件开发过程的一个周期性过程。

其主要流程为：

1. 开发
2. 判断是否过时，如果过时则跳到步骤5
3. 使用软件
4. 修改软件，跳到步骤2
5. 停止该软件的维护

其中，判断软件是否过时指的是：该软件效率低下，语言过时，或者用户需求出现巨大变更等使得软件失去了其有效性。

### 开发过程模型

开发过程包括了：分析，设计，实现，测试四个阶段。这四个阶段是按顺序进行的。

而常见的开发过程模型有如下两种。

#### 瀑布模型

瀑布模型指的是一次性全量的完成四个阶段的事情。也就是完整的分析，然后再完整的设计，etc。

瀑布模型的缺点在于其无法适应需求变更的场景。当在开发过程中出现需求变更或需求不合理的情况的时候，需要回过头来重新从分析阶段开始修改。

#### 增量模型

增量模型是指将一个开发项目拆分成许多个小的需求，并分别进行分析，设计，实现，测试。

这相当于每个需求都是前一个需求的增量，开发项目是在不断增量的完成的。

其优点就是可以适应需求变更场景。

## 分析阶段

这个阶段需要做的事情就是定义**软件能够做什么**，不需要说明软件如何去做。

分析阶段有两种分析方式。

### 面向过程分析

简单的将就是用面向过程的思维进行分析，将所有的事情都看作是过程调用。

其会用到的主要工具有：

+ 数据流图
+ 实体关系图
+ 状态图

### 面向对象分析

相对的，这个就是使用面向对象的思维进行分析，将所有的对象提取出来并为此设计满足需求的方法。

其会用到的主要工具有：

+ 用例图
+ 类图
+ 状态图

## 设计阶段

在这个阶段就需要明确软件如何去做了。

同样的，其分为面向过程设计和面向对象设计两种。

### 面向过程设计

在面向过程设计中，整个系统会被分解为一系列的过程或者模块。

其主要会用到结构图来展示模块化。

在模块化的过程中就需要注意需要尽可能的**低耦合高内聚**。

简单的讲就是注意模块内功能的高度内聚和模块之间的低相关性。

### 面向对象设计

在面向对象设计中，整个系统被看作是许多的类以及其交互来进行设计的。

类与类之间同样需要遵循低耦合高内聚。

## 实现阶段

这个阶段就是根据设计阶段得到的结果进行实现。

在实现过程中需要注意的最多的就是**软件质量**问题。

软件质量的指标包括：

+ 可操作性
  + 准确性：错误和用户的请求变更越少越好，最好是没有
  + 高效性：软件性能的高效
  + 可靠性：简单的讲就是降低故障的发生频率
  + 安全性：非授权人员得到系统数据的难易程度
  + 及时性：软件完成任务的时效性
  + 适用性：用户适应这个软件的使用
+ 可维护性
  + 可变性：其是否需要经常面对需求变更
  + 可修正性：发生故障时的修复难易程度
  + 适应性：用户变更需求的时候的修改难易程度
  + 可测试性：测试的难易程度
+ 可迁移性
  + 重用性：模块/类在不同项目或需求中的可重用性
  + 互用性：模块/类跟数据或其他的模块/类的交互能力
  + 可移植性：程序从一个平台移植到另一个平台的难易程度

## 测试阶段

当程序写好的时候就进入了测试阶段。显然这个阶段就是为了测试程序的功能。

### 白盒测试

简单的讲就是在知道程序的构造的情况下进行测试。

其主要有：

+ 基本路径测试：使用不同的执行路径将程序中每一条语句都测试运行一遍
+ 控制结构测试：只测试每个控制结构是否能正常运行。这个就包括了基本路径测试能测试到的范围了
  + 条件测试：测试每个条件语句的所有分支是否能正常进入
  + 数据流测试：测试每个赋值语句是否能正常赋值
  + 循环测试：测试每个循环是否能正常运作

### 黑盒测试

简单的讲就是在不知道/装作不知道程序构造的情况下进行测试。

这种测试只关心程序是否能按照正常的输入得到需要的输出。

其主要有：

+ 穷尽测试：将所有可能的输入都测一遍。这显然吃力不讨好
+ 随机测试：在穷尽测试的测试集中随机取测试用例构成子集进行测试
+ 边界值测试：使用一些边界输入进行测试

一般会使用随机测试+边界值测试

## 文档

一个软件需要文档来支撑其使用/维护。

其主要有：

+ 用户文档：让用户知道如何使用该软件
+ 系统文档：定义软件本身
+ 技术文档：描述软件的安装/维护/更新
