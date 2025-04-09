# TGM4 Master模式规则简述与推荐策略

> 部分信息来自wiki，策略来自个人经验和脑测，仅供参考，随时可能更新

> 仅供在各大wiki内容补充完整之前临时参阅，准确内容还是见各大wiki，等大家把规则挖得差不多了之后本仓库会archive

## 分数计算

### 基础

1. 每一块锁定并完全结算后（下一块出生前的瞬间）+1分
2. 消除1/2/3/4行加1/2/3/6分

### 奖章加成

游戏场地右边有四种特殊动作的计数器，这四种动作会带来分数加成和铁块转化延迟：

| 动作   | 分数加成   | 额外冰冻块转化延迟   |
| ------ | ---------- | -------------------- |
| 全消   | 每6个+1    | 每个+2.5帧(向下取整) |
| 消四   | 每10个+1   | 每个+1帧             |
| T2或T3 | 每16个+1   | 每个+1帧             |
| PIKII  | 达到28后+1 | 每个+3帧             |

## 玩法规则

### 20G

基础玩法，锁延随每100分缩短，难度增加

### 锁延刷新条件

本模式中，最开始有16次移动重置和4次旋转重置机会，方块下移时恢复这两个次数，但每一块最多总共重置128次

1200分后移动和旋转不再重置锁延，只有下移时刷新

### PIKII

在前1000分中，分数的百位是3/5/7/8/9时，场地的下十行会被锁定，填满了行不会消除（分数照加），**填满每行时获得一个PIKII奖章**

过百时填满的PIKII行会立刻一起消除

### Cyclone(随机朝向)

从1000开始，方块的出生朝向随机，并且只能在hold或第一next中看到（第二next后的块还是显示为正常朝向）

### Master PIKII

从1300开始，放置的方块会在消除结算后转化为冰冻块，冰冻块不可消除，且包含冰冻块的行在消除后，上方的行不会下落

方块转化为冰冻块的延迟可以靠奖章增加（练习模式直接1300开的话没有奖章就是立刻转化），如果前1000打得不完美的话基本就是到killscreen了，别想着通关

消四时会强制消除场地最底部一行，包括冰冻块（唯一消除冰冻块的方法，但是要做消四本身也慢了，其实也没啥用…？）

### 字幕战

到达2600分后进入最终字幕战

游戏会撤回最后放置的150块（像asuka模式一样倒带），然后要求在65s内重新达到2600分

### 段位

| 进度       | 段位                 |
| ---------- | -------------------- |
| 达到1100   | Master               |
| 死在字幕战 | Grand-Master         |
| 通关字幕战 | Grand-Master! Rounds |

## G-M!R的策略

### 前1000

前1000尽量做到“完美”：
- 前期低难度的时候多做点T2，得分效率也低，多拿一点转化延迟为冰冻块做准备
  - 拿都拿了就顺便做到16个把分数加成也拿了吧
- 打满所有PIKII段落，共50行
- 尽量多消四

此时冰冻块转化延迟大约接近200帧，也就是3秒多：
- PIKII 150f，这是最主要的
- T-spin 约16f
- 消四 约30f

同时你有约+5的额外得分：
- PIKII +1
- T-spin +1
- 消四 +3

### 1000~1300

1000后难度过高了，就不要求完美了，看着打吧，能捡几个T2或者消四最好

### 1300~2600

1300开始冰冻块段落，尽量把速度拉起来，在转化成冰冻块之前消掉，这是得分最快+可持续的方案

假设之后都消一得6分，平均算下来每一块得3.4分，需要放约400块到达2600

### 字幕战

可以起1+2+3wide：  
1wide的部分约五六格，用来消四  
2wide的部分2~3格，再多就不好算了  
3wide的部分任意高，看你控制

这个堆叠可以比较容易地无限往里丢块，消除所有非冰冻格，比较接近循环流程，得分速度也极其快，目测应该是最终解决方案

不过在一些消四后这个形状会变矮，所以也需要额外进行一些地形调整，只能多练了
