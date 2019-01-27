- 资料来源

  - <https://classroom.udacity.com/courses/ud730/lessons/6370362152/concepts/63798118160923>

- 文章作者：Stevenkcolin

- 深度学习课程组成

  - simple model from end to end, includes:
    - Logistic Classification 聚类问题
    - Stochastic Optimization 优化
    - Data & Parameter tuning  数据和参数调整
  - Deep Learning Network
    - Build first Deep Learning network
    - Regularization 正则化优化
  - Image & Convolutional models 图像识别和卷积分网络
  - Embedding & Recurrent models 嵌入和循环网络

- 神经网络历史

  - 80年代-90年代是神经网络的高潮，LeCun曾经用神经网络实现了简单的识别数字功能
    - 但当时的计算能力和存储能力不够
  - 90年代末到2000年初的时候，是神经网络和人工智能的低潮期（此时最流行的应该是计算机技术的应用层面）
  - 到2009年开始神经网络又再次盛行起来
    - 2009: 语音识别
    - 2012: 图像识别
    - 2014: 机器翻译
    - 理由：海量的数据 + 便宜的CPU

- 回顾机器学习的基本内容

  - 分类问题

    - 必须有features和examples
    - 需要有training sets, validation sets, test sets

  - Classification 是所有机器学习解决问题的基础，从他可以衍生出其他问题

    - 回归，典型的如线性回归
    - Ranking，排序问题
    - Detection，侦测，比如马路上的图像识别
    - Reinforcement Learning：增强式学习

  - 举个例子

    - 如果你的无人驾驶汽车，如何判断前面是否有人
      - 方法就是对面前的图像不断进行分类，判断前方是否有人这种分类

  - 再来个例子

    - 搜索的过程如何使用人工智能

      答案：方法很简单，就是把所有的可能结果都分类成（和你的搜索问题）是有关，还是无关两种分类。这样你的体验就会很好了。

      比如：你搜索 赵丽颖和冯绍峰，那么和他们有关的内容有

      - 知否知否电视剧
      - 两人有孩子
      - 两人结婚
      - 各自的娱乐行业发展情况
      - 和他们重名的冯绍峰，比如是个教授，或者大学老师的新闻（这个关联度最低），所以会排在最后

- 线性回归

  - 经典问题

  - $$
    y = WX + b
    $$

    W=Weight

    B = bias 偏差

    X是一个巨大的矩阵

    y是一个向量

  - 我们训练的目的是为了找出最合适的W & b

  - 线性回归同城会遇到两个典型问题

    - 高偏差
    - 高方差
    - 如果能够将偏差和方差平衡在一个很好的点上的话，那么我们的训练就很成功

- SoftMax

  - 可以将数据转化成possibility，而且高分对应的是高概率，低分对应的是低概率
  - 所以softmax是一个很好的$g(z)$

- OneHot 编码

  - 这个是特征工程的一部分
  - ![image-20190127130234783](https://ws2.sinaimg.cn/large/006tNc79gy1fzl24ho05nj30hv0dijt7.jpg)

- 交叉熵
  - ![image-20190127130443831](https://ws3.sinaimg.cn/large/006tNc79gy1fzl26p0f9yj314w0nbajm.jpg)
  - 整个线性模型的流程可以认为是这样的
  - ![image-20190127130555643](https://ws4.sinaimg.cn/large/006tNc79gy1fzl27y99zaj31740nxam5.jpg)
  - 以上的方法被称为：
  - Multinomial Logistic Classification

- 线性回归的基本逻辑，用两张图就可以解释

  - 我们需要求值最小，而里面的内容我们已经都有了包括

    - $$
      x_i \quad 数据初始化\\
      D \quad 开始的交叉熵 \\
      S \quad softmax 代码 \\
      L_i \quad one-hot编码 \\
      \\
      我们所求的就是 W 和 b
      $$

      

![image-20190127132345392](https://ws1.sinaimg.cn/large/006tNc79gy1fzl2qhxva2j30zo0nhdr7.jpg)

- 方法及时反向传播算法
  - ![image-20190127132805660](https://ws2.sinaimg.cn/large/006tNc79gy1fzl2v05l7gj312l0mtn5s.jpg)

- 数据三种集合
  - training sets
  - validation sets
  - test sets
- Validation Sets
  - Validation Sets > 30,000 examples
  - Changes > 0.1% in accuracy



- ## Stochastic Graident Descent

  - S.G.D 深度学习的核心 （随机梯度下降）
  - Inputs
    - means 平均值
    - equal variance
  - Initial Weights
    - Random
    - MEAN
    - Equal Variance
    - Momentom 动量
    - Learning Rate Decay 学习曲线下降
  - High Learning Rate
  - Low  Learning Rate

- 调参方法论

  - Iniitial learning rate 学习率
  - learning rate decay
  - Momentum
  - Batch size
  - weight initialization
  - 
  - 
  - 当发生意外的时候，首先想到的是降低learning rate
  - 

- ADA Grad 方法

  - 可以减少前三个3问题，急需要收到·weight & batch size的影响

  