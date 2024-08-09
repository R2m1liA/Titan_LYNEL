[TOC]

# 《塞尔达传说：旷野之息》 怪物分析——莱尼尔

## 怪物简述

莱尼尔（以下简称**人马**）是《塞尔达传说》系列中出现的敌人，其最早登场于初版《塞尔达传说》的死亡之山上，往往成群分布，在死亡之山上阻击林克。可见彼时的莱尼尔的定位还更接近于小怪而非精英或Boss。《塞尔达传说：旷野之息》（以下简称**《旷野之息》**）中登场的人马，则被塑造成了一个实力强劲的精英敌人，其为浑身长有鬃毛的半人马形象，简陋的护甲无法掩盖其壮硕的身材，存在手持**剑盾，大剑、长枪**的三类，无论是哪一种人马，其带给玩家的印象都是——这是一个需要认真对待的对手。

![人马莱尼尔——来自美术设定集](pic\人马莱尼尔——来自美术设定集.png)

在《旷野之息》中，人马的战斗体验可以用**大开大合，堂堂正正**来形容，人马的所有招式，均有较为明显的前摇，大开大合的招式带给玩家独特的战斗体验。玩家与人马的战斗往往以**见招拆招**为主。

## 形象设计

莱尼尔的形象可以很明显的看出半人马与狮子的设计原型，在整体呈现半人马外观的情况下，上半身长有大量狮子般的鬃毛。身上带有历战的伤痕，穿有简单的护甲。从其形象设计中也可以对其战斗风格略知一二：半人马的下身可以使它在战场上快速游走发起攻击，鬃毛与肌肉揭示了其带有力量感的攻击方式。整体是一只敏捷且富有力量感的精英敌人。

## 战斗设计

《旷野之息》中人马的战斗可大致分为两个阶段：**索敌阶段**与**战斗阶段**

### 索敌阶段

人马的索敌拥有非常大的索敌范围，索敌范围可分为三个部分：以人马为中心，由外向内分别为**视野范围**、**警戒范围**与**攻击范围**。当玩家处于不同的索敌范围内时，人马会有不同的行为。

![image-20240730171743105](pic\image-20240730171743105.png)

#### 视野范围

当玩家进入人马的视野范围一定时间后，人马发现玩家，但其不会立刻对玩家发起攻击，而是在**原地**与玩家对视（以下称为**注视状态**），等待玩家的下一步行动，视玩家的不同行为，其会做出不同的反应。

- 玩家继续前进，进入警戒范围，此时人马拔出武器，进入**警戒状态**，但是依旧不会对玩家立刻发动攻击，而是依旧在原地等待玩家的行动
- 玩家在视野范围内拔出武器，人马同样拔出武器，进入**警戒状态**，但是依旧不会对玩家立刻发动攻击，而是依旧在原地等待玩家的行动
  - 玩家在视野范围内挥动武器，AI判断玩家做出攻击行为，人马立刻进入**战斗状态**，向玩家发起攻击
- 玩家长时间未做出任何行动，人马拔出武器，进入**战斗状态**，对玩家发起攻击

#### 警戒范围

玩家进入人马的警戒范围，人马拔出武器，进入**警戒状态**，但其不会立刻对玩家发起攻击，而是依旧在原地等待玩家的行动，视玩家的不同行为，其会做出不同的反应。

- 玩家继续前进，进入**攻击范围**，人马立刻进入**战斗状态**，对玩家发起攻击
- 玩家在警戒范围内拔出武器，人马立刻进入**战斗状态**，对玩家发起攻击
- 玩家长时间未做出任何行动，人马进入**战斗状态**，对玩家发起攻击
- 玩家退出警戒范围，回到**视野范围**，人马会将拔出的**近战武器**收回，并将所持武器切换为用于远程攻击的**弓箭**

#### 攻击范围

玩家进入人马的**攻击范围**，人马立刻进入**战斗状态**，对玩家发起攻击

- 当人马进入**战斗状态**时，视其手持武器的不同，会有不同的行为模式

![莱尼尔索敌状态转换图](pic\莱尼尔索敌状态转换图.png)

总的来说，人马的索敌机制可以概括为：**若玩家对其没有明显的敌意，则人马不会主动攻击玩家**；是个堂堂正正的斗士。

### 战斗阶段

当莱尼尔个体种类不同、持有不同类型的武器不同时，其行为模式会有细微的区别，因此这里仅以持有**剑盾**的**白银人马**为例进行分析

#### 战斗状态
根据上文的索敌逻辑可以看出，人马进入战斗时会有两种不同的状态：**战斗状态（近）**与**战斗状态（远）**。

- 当人马进入**战斗状态（远）**时，其使用**弓箭**进行战斗。当玩家没有主动接近人马时，其会停留在原地使用弓箭攻击玩家，而当玩家主动接近人马时，人马也会开始向玩家移动，并在达到近战返回后切换为**战斗状态（近）**
- 当人马进入**战斗状态（近）**时，其使用**剑盾**进行战斗。在人马进入近战距离后，由于人马移动速度较快，如果没有特殊的移动手段，玩家很难双方距离再拉至远程范围

#### 技能设计

由于人马的技能与技能之间并没有明显的派生关系，并且其技能使用与**人马和玩家之间的相对位置**有一定的相关，因此以下招式分析采用**近距离、中距离、远距离**的距离分类

![莱尼尔技能](pic\莱尼尔技能.png)

##### 近距离

人马在近距离时主要使用手上的近战武器进行战斗

###### 咆哮& 砸地

人马首先在原地进行咆哮（仅有视觉效果、无伤害），然后使用手上的武器进行砸击地面，在以自身为中心的一定范围内形成爆炸

- 当人马由**近战形态**进入战斗时，大概率直接使用该技能
- 砸地形成的爆炸会使周围温度上升（着火）

###### 三连斩击

人马抬起右手上的近战武器，向玩家方向发动三次横向斩击

- 每次斩击都带有一定距离的位移（距离很短）
- 每次斩击的前摇阶段会根据**玩家位置**进行攻击方向修正（修正角度较小）

###### 钳击

人马抬起双手，向玩家发动由两侧向中间的夹击

- 攻击带有一定的位移（距离较短）
- 攻击的前摇阶段会根据**玩家位置**进行攻击方向修正（修正角度较小）

##### 中距离

人马在中距离可能会尝试直接接近玩家，或者使用突进技能、部分远程攻击技能

###### 突进

人马拥有三类**突进型技能**，能够快速接近玩家

- 持剑突进：人马举起右手武器，向玩家发起速度较快的冲锋
- 跑攻：人马举起右手武器，以较快速度（比突进慢）接近玩家并发起攻击
- 肉身突进：人马凭借肉身，向玩家发起速度较快的冲锋

值得注意的是，人马在**近距离**时也有可能使用突进技能，此时人马会先尝试拉开与玩家的距离，然后向玩家突进。拉开距离的动作具有较明显的**目标选择**规律，即**玩家摄像机正前方一定距离**，若有中途被阻挡，则会在碰到障碍物后立刻使用突进技能。

![突进位置修正](pic\突进位置修正.png)

###### 跳跃下砸

人马跳起后向使用右手武器向玩家位置发起砸击，同样可以接近玩家

- 使用频率很低，推测为**无法使用突进技能**接近玩家时才会使用的技能

###### 三连火球

人马向玩家依次发射三枚火球进行攻击

- 火球会时路径上的区域温度上升（着火）
- 每次发射火球均会根据**玩家位置**进行方向修正
- 在**近距离**时也有概率使用，在使用之前会先进行后跳，后跳方向为**人马正后方**

##### 远距离

在远距离时，人马会使用弓箭向玩家发起工具

###### 弓箭射击

人马举起弓箭，在蓄力一定时间后向玩家发射三枚弓箭

- 根据人马类型不同，发射的箭矢种类也有所不同
- 三枚弓箭同时射出，并在水平方向上呈一定的夹角，中间的箭矢朝向玩家

- 在人马持弓接近玩家时也会进行蓄力

###### 曲射

人马抬起弓箭，在蓄力一定时间后向天空发射箭矢，箭矢在一定时间后落向玩家位置

- 当人马与玩家之间存在阻挡，**无法直接使用弓箭命中**玩家时会使用

#### 弱点

人马拥有一个弱点——他的**眼睛**，当玩家使用弓箭击中他的眼睛使，会使它陷入较长时间的硬直，玩家可以趁着硬直时间对人马发动攻击。

### 战斗场地

作为一只难度较高的精英敌人，人马在游戏中分布较为分散，且往往**单独**出现在较为**空旷的地带**，且周围**鲜有小型敌人出没**。因此，玩家在与人马进行战斗的过程中，可以将注意力集中在人马本身之上。同时，与人马的对战也缺乏环境交互手段，因此其更加考验玩家自身的能力使用。

### 战斗设计简评

从上述内容中可以看出，人马具有丰富的战斗技能与相当优秀的AI设计。这样的设计鼓励玩家正面应对人马，虽然招式繁多但多数有迹可循，能够较为简单地应对。对玩家来说，人马虽然难度较高但称不上难以对付，在练习一段时间后可以较为熟练地击杀。在《旷野之息》中，人马是一只设计非常优秀的精英怪。



# 人马型泰坦LYNEL——对莱尼尔的重新设计

## 《泰坦之魂》的游戏特征分析

在对《旷野之息》中的怪物莱尼尔进行重新设计，使之适用于《泰坦之魂》前，需明确《泰坦之魂》的游戏特征，依次首先对目标游戏特征进行简要分析

《泰坦之魂》的战斗玩法的特征可以概括为：**一触即发、一击毙命快节奏战斗**，根据此特征设计出的游戏内的敌人——**泰坦**，则具有以下特征：**拥有单一弱点**、**快速的出招速度**、**较为简单的战斗AI**、**古老、巨大**

### 战斗系统：一触即发、一击毙命快节奏战斗

《泰坦之魂》中的主角没有生命值的设计，这意味着一旦主角被泰坦击中便会死亡，同样的，泰坦也会被玩家一击毙命。泰坦的攻击多种多样，而主角只有一把弓和**一根箭矢**，主角每次射出箭矢，都需要花费时间将其收回，这意味着主角的每次攻击都将导致他暂时失去主动进攻的能力。玩家需要再泰坦猛烈而快速的进攻中找到能够命中其弱点的时机，射出箭矢将其一击毙命。这样的机制带来的是快节奏的战斗与较低的容错率。

### 怪物设计：单一弱点

《泰坦之魂》的怪物设计的一个明显的特征就是：其怪物均**具有单一的弱点**。游戏要求玩家使用箭矢命中敌人的弱点方可击败敌人。怪物的弱点往往受到保护，仅在招式与招式之间的缝隙能能够找到命中弱点的时机。例如游戏中的巨像GOL-IATH，其弱点为胸口，而胸口的弱点被一只手护住，玩家需要引导其换手攻击并在换手的间隙内将其击破。

![巨像GOL-IATH](pic\巨像GOL-IATH.png)

### 怪物设计：快速的出招速度

前面说到，游戏的战斗时一击毙命的，自然不能让玩家能够轻易命中泰坦的弱点。那么，为了增加玩家游玩时的紧张感，游戏的敌人在设计上普遍拥有较快速的出招、收招速度，更快的出招速度带来的是更短的决策时间，通过使玩家**“躲避攻击”**的操作更加频繁，从而提高玩家进行**“瞄准弱点”**操作的成本。

### 怪物设计：较简单的战斗AI

《泰坦之魂》中的怪物技能较少，同时AI较为简单。以上文提及的巨像GOL-IATH为例，其能够使用的技能仅有**出拳下砸**与**换手**：当玩家与攻击手处于同侧时，巨像使用出拳下砸，当玩家与攻击手处于异侧时，巨像进行换手。游戏中，怪物的技能基本按照**固定序列**释放，不与玩家或者环境相关。这样的设计能够让玩家在多次挑战怪物后能够在一定程度上预测、引导怪物的出招。从而让玩家更加快速的击败怪物

### 怪物设计：古老、巨大

《泰坦之魂》中的泰坦，尽管形态各异，但是他们都有一个共同特点，那便是古老而巨大——只有足够悠久，才有成为泰坦的资格。尽管有The Soul这样与主角同样体型的敌人，但是绝大部分泰坦无一例外都是巨大的造物、生物，体型往往数倍与主角，渺小的主角与巨大的泰坦的战斗展现出一种史诗感。

## 设计思路

根据上文总结出的《泰坦之魂》的游戏特征，对《旷野之息》中的**莱尼尔**进行进行以下设计，将其设计为**人马型泰坦**，从而适用于《泰坦之魂》

- 重新设计形象：略微**调整人马形象**，凸显其古老感。原作游戏中以眼睛为弱点的设计放在《泰坦之魂》中会显得弱点不明显，因此**调整弱点位置**：考虑调整至腹部。

- 简化战斗逻辑：《旷野之息》中的人马具备相当优秀的战斗AI，而这样的AI对于《泰坦之魂》来说是**过于复杂**的，因此需要**简化其战斗逻辑**，将其战斗修改为若干不同技能的顺序释放。

- 战斗场地：泰坦应当由与之相匹配的**战斗场地**，在完成怪物设计后，应当为其设计合适的战斗场地。

## 形象的重新设计

伤痕是历战的证明，为了凸显LYNEL的悠久感，相比于《旷野之息》中的莱尼尔，LYNEL具有更加明显的**伤痕**。浑身拥有大大小小伤痕的LYNEL，其最严重的伤痕位于腹部，与其说是伤痕，不如说是空洞，已然可以透过表面看到内脏，这是LYNEL身上最脆弱的部分，只要将箭矢射入腹部，便可将其击败。将身上最脆弱的部位正对着敌人，符合其堂堂正正的斗士形象。

![泰坦LYNEL](pic\泰坦LYNEL.PNG)

## 战斗逻辑设计

### 简化攻击手段

《旷野之息》中的人马具有近战与远程两种不同的武器，在重新设计后，考虑去除近战武器，仅保留用于远程射击的**弓箭**。LYNEL将依靠他的**肉体**对玩家进行近身攻击。手持弓箭的LYNEL在一般状态下**自然护住腹部的弱点**

### 技能

经过简化后的怪物仅保留三个技能：**咆哮**、**冲锋践踏**与**弓箭射击**，同样是既有远程攻击手段又具备近战攻击手段

#### 咆哮

LYNEL张开双臂发动咆哮，震撼附近的一切生物

- 咆哮对以自身为中心，一定半径内的**圆形区域**发动
- 咆哮不对玩家造成伤害，但是会**击飞玩家**，使玩家向反方向位移，若将玩家击飞至**场地边缘**，则玩家**死亡**
- 咆哮会**暴露**LYNEL腹部的弱点，但是咆哮掀起的风压会**击落箭矢**，使其无法击中弱点

![LYNEL-咆哮](pic\LYNEL-咆哮.png)

#### 冲锋践踏

LYNEL向玩家发起冲刺，并在玩家位置进行践踏

- 冲锋以玩家为目标，冲锋过程中会对路径上的玩家造成伤害
- 冲锋距离取决于与玩家的距离，冲锋过程中**不进行方向修正**
- 冲锋结束后进行践踏，LYNEL抬起前蹄，将身位修正为**面向玩家**，并落下前蹄，会对自身周围的玩家造成伤害

![LYNEL-冲锋践踏](pic\LYNEL-冲锋践踏.png)

#### 弓箭射击

LYNEL使用弓箭向玩家射出箭矢

- 箭矢与原作相同为三向箭矢
- 三向箭矢中，中间位置的箭矢向玩家射击
- 根据游戏难度不同，可能会出现连续射击的情况，每次射击均会修正射击方向

![LYNEL-弓箭射击](pic\LYNEL-弓箭射击.png)

### 战斗场地

LYNEL的战斗场地呈现**圆形**，战斗未触发时，LYNEL处于场地正中央，当玩家射出箭矢碰撞LYNEL时，战斗开始，LYNEL向玩家发起攻击。战斗场地内没有任何用于阻挡的障碍物。整体风格可参考**罗马斗技场**

![Anfiteatro,_El_Jem,_Túnez,_2016-09-04,_DD_11](pic\Anfiteatro,_El_Jem,_Túnez,_2016-09-04,_DD_11.jpg)

### 行为逻辑与交战流程

作为《泰坦之魂》中的怪物，LYNEL具有相对简单的行为逻辑：LYNEL的技能释放遵循**固定序列循环释放**的原则，每次技能释放都仅与**玩家位置**相关

#### 交战流程

从战斗开始为准，LYNEL将会依次释放**咆哮->冲锋践踏->弓箭射击->咆哮->冲锋践踏->冲锋践踏->弓箭射击**，在战斗过程中依次循环释放技能轴上的技能

![LYNEL技能轴](pic\LYNEL技能轴.png)

LYNEL战斗的交战流程很简单：在技能轴期间躲避敌人的攻击，并抓住露出弱点的窗口击败敌人即可。根据上文所述的技能设计，可知弱点窗口位于技能轴中的两次咆哮之后，咆哮的风压消失后的短暂时间内，玩家可以对其进行攻击。

![LYNEL弱点窗口](pic\LYNEL弱点窗口.png)

### 困难模式

《泰坦之魂》中困难难度的敌人相比普通难度在机制上不会有很大的变化，难度的提升主要体现在敌人的技能变得更加**快速、频繁**。并且在技能使用上与普通难度有着细微区别。基于上述原则对困难难度的LYNEL的技能做以下调整：

- **咆哮：**咆哮范围**增大**；收招加快，即暴露弱点的时间**缩短**
- **冲锋践踏：**冲锋速度**加快**；践踏范围**增大**
- **弓箭射击：**箭矢速度**加快**；可能连续射击2-3次（根据技能轴安排而定）

#### 技能轴(困难)

对普通难度LYNEL的技能轴进行调整

![LYNEL技能轴（困难）](pic\LYNEL技能轴（困难）.png)

调整后的技能轴在两次**冲锋践踏**之间加入了一次**弓箭射击**；同时，不同位置的弓箭射击会连续射出不同次数的箭矢。这样的更改可以使得LYNEL的技能释放在表现上更加**频繁**与**激进**，尽管实际修改并不多。由于**咆哮**带来的弱点窗口更短，因此要求玩家拥有更强的把握时机的能力。



以上为对《旷野之息》中的怪物莱尼尔进行重新设计，使其成为适用于《泰坦之魂》中的泰坦LYNEL的设计方案。
