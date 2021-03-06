﻿# Excel数据分析 第五课

标签（空格分隔）： Excel数据分析

---
# 1 . 对练习5.xlsx的两个数据集画直方图，并说说你觉得这两个数据集应该是什么分布

 - 数据集1 
    - 描述了在一个单位时间内，生成了500个随机变量，即发生了500个随机事件，其中随机事件的分布集中在[20,50]这个区间，其余区间的数字相对较少,可以认为符合正态分布。
 - 数据集2 
     - 从图像与数据特征上来看，近似于正态分布。



# 2. 本周学习了几种常见的数据分布，你能找出哪些现实场景中的数据会是这几种分布中的一种？

- 离散概率分布 
    - 二项分布 
        -  如果该事情发生次数固定，而你感兴趣的是成功的次数，那么就可以用二项分布的公式快速计算出概率来。
    1）做某件事的次数（也叫试验次数）是固定的，用n表示。（例如抛硬币3次，投资5支股票）
    2）每一次事件都有两个可能的结果（成功，或者失败）（例如每一次抛硬币有2个结果：正面表示成功，反面表示失败。每一次投资美股有2个结果：投资成功，投资失败）。
    3）每一次成功的概率都是相等的，成功的概率用p表示（例如每一次抛硬币正面朝上的概率都是1/2。
    4）你感兴趣的是成功x次的概率是多少。那么就可以用二项分布的公式快速计算出来了。（你已经知道了我前面讲的5家美股的赚钱概率最大，所以你买了这5家公司的股票，假设投资的这5家公司成功的概率都相同，那么你关心其中只要有3个投资成功，你就可以赚翻了，所以想知道成功3次的概率）

 - 几何分布
     - 如果你需要知道尝试多次能取得第一次成功的概率，则需要几何分布。
1）做某事件次数（也叫试验次数）是固定的，用n表示（例如抛硬币3次，表白5次）
2）每一次事件都有两个可能的结果（成功，或者失败）
3）每一次“成功”的概率都是相等的，成功的概率用p表示
4）你感兴趣的是，进行x次尝试这个事情，取得某1次成功的概率是多大。

 - 泊松分布
     - 如果你想知道某个时间范围内，发生某件事情x次的概率是多大。
1）事件是独立事件（之前如果你看过我的《投资赚钱与概率》已经知道赌徒谬论了，所以类似抽奖这样的就是独立事件）
2）在任意相同的时间范围内，事件发的概率相同（例如1天内中奖概率，与第2天内中间概率相同）
3）你想知道某个时间范围内，发生某件事情x次的概率是多大（例如你搞了个促销抽奖活动，想知道一天内10人中奖的概率）
一个医院中，每个病人来看病都是随机并独立的概率，则该医院一天（或者其他特定时间段，一小时，一周等等）接纳的病人总数可以看做是一个服从poisson分布的随机变量

 - Poisson分布的第一个定义是一个随机变量X
 - 只能取值非负整数（x=0,1,2,...），且相应的概率为，则该变量称为服从poisson分布。
 - 这个定义就是我们平时考试或者理论工作时用的poisson随机变量的定义。
 - 注意Poisson还有一个知名度比较小的第二个定义，或者说是Poisson Process的定义：
    - 假定一个事件在一段时间内随机发生，且符合以下条件：
        - （1）将该时间段无限分隔成若干个小的时间段，在这个接近于零的小时间段里，该事件发生一次的概率与这个极小时间段的长度成正比。
        - （2）在每一个极小时间段内，该事件发生两次及以上的概率恒等于零。
        - （3）该事件在不同的小时间段里，发生与否相互独立。
        - 则该事件称为poisson process。
    - 回到医院的例子之中，如果我们把一天分成24个小时，或者24x60分钟，或者24x3600秒。时间分的越短，这个时间段里来病人的概率就越小（比如说医院在正午12点到正午12点又一毫秒之间来病人的概率是不是很接近于零？）。条件一符合。
    - 另外如果我们把时间分的很细很细，是不是同时来两个病人（或者两个以上的病人）就是不可能的事件？即使两个病人同时来，也总有一个人先迈步子跨进医院大门吧。条件二也符合。
    - 倒是条件三的要求比较苛刻。应用到实际例子中就是说病人们来医院的概率必须是相互独立的，如果不是，则不能看作是poisson分布。
    - 题主的问题是为什么现实生活中的情况（如医院例子）会服从poisson分布的第一定义。
    - 现在有了第二定义作为桥梁，应该就很容易理解了。
    - 现实生活中的例子中如果事件相互独立，那么它就是符合poisson分布的第二定义的。
    - 而从poisson第二定义到poisson第一定义之间是有严格的数学证明的。
![image_1c038bt531oegcfvstis1t20ap.png-80.3kB][1]
![image_1c038ccjp105v1tg07epr7cncu16.png-85.1kB][2]
![image_1c038cn881iur15dk2eqhqa1o411j.png-41.8kB][3]

案例:
二项分布：抛10次硬币，硬币向上的概率概率
几何分布：抛10次硬币，第3次硬币向上的情况
泊松分布：以抛硬币10次为一组，每一组发生第3次硬币向上的概率

 - 连续概率分布
    - 正态分布
正态分布是一种连续型随机分布，它由两个参数决定，一个是均值，一个是方差
当中心极限定理出现之后，有一个非常重要的结论：大量独立同分布的随机事件，整体上服从正态分布。

一个班或者一个年级的学生考试，这个班的成绩高分段和低分段占少数，而大部分学生的成绩都集中在中间分数段，也就是大部分学生的成绩都集中在平均分（比如75）左右，并且高于平均分的分布和低于平均分的分布应当是基本一致的（对称）。所以这个班的考试成绩符合正态分布

  [1]: http://static.zybuluo.com/419145138/7f3fotf41yr76iwuj7knubmu/image_1c038bt531oegcfvstis1t20ap.png
  [2]: http://static.zybuluo.com/419145138/vny6hf5x9owhvt4yb2cjpioj/image_1c038ccjp105v1tg07epr7cncu16.png
  [3]: http://static.zybuluo.com/419145138/r71ug01rlvi4gh6chxhfs22b/image_1c038cn881iur15dk2eqhqa1o411j.png