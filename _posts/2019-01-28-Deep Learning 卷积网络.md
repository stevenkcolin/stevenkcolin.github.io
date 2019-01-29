# Deep Learning - 卷积网络





## 卷积网络

1. CNN Convolutional Neural Networks，或者说Connets

2. 简单的说就是在Neural Networks的基础上增加一个卷积来优化神经网络。

3. 理由：

   1. 主要是以往的神经网络在处理问题的时候会遇到数据维度过大，
      1. 比如一张图片 $100 * 100 * 3 color$ = 30000个features。
      2. 而如果图片是1080p, 那么就是 $1080*720*256$ 基本上就是个天文数字的矩阵，用它来进行神经网络训练去判别图片，计算量是无法满足的

   

## 卷积层 Conv

- 用一个卷积分层，作为一层神经网络，将原始数据做变形，变得更小但更厚。

- 如图所示：

![image-20190129142021490](https://ws2.sinaimg.cn/large/006tNc79gy1fznfm2wea9j313g0lwtlk.jpg)



- 如上图所示
  - $256*256*RGB$ 是我们的输入。
  - 最后很小的Classifiers * 相应的矩阵就是一个输出，判断我们属于那种分类（Classification）比如狗或者猫，车子或者人。等等



## Pooling 池



#### Max Pooling

- Advantage
  - Prameter Free
  - Often more accurate
- Disadvantage
  - More Expensive
  - More Hyper Parameters



- 



## 一个卷积网络例子

#### 机器学习三巨头之一的Yann Lecun 98年提出 

![image-20190129143544128](https://ws1.sinaimg.cn/large/006tNc79gy1fzng20wkc2j31460jtwu5.jpg)



上面是一个理论例子，再来看一个典型的图像识别的实操例子：

![image-20190129144031870](https://ws1.sinaimg.cn/large/006tNc79gy1fzng70jt15j30xe0jhndi.jpg)



#### 对于工程领域（也就是IT行业来说），实际上就是对大牛论文的代码实现

#### 从上图可以看出

$$
FC = Full Connected \\
Result = Relu(Conv_1,Conv_2) + Pool + Relu(Conv_3,Conv_4) + Pool + Relu(Conv_5,Conv_6) + FC
$$



然后这个卷积网络就能判断出是car的概率很高，然后就输出是个Car





## 具体实现上的一些概念

- Input Depth
- Output Depth
- Stride
- Feature Map
- Kernel
- Valid Padding
- Same Padding
- FC = Full Connected
- Max Pool
- 残差



## 一个Google图像识别的例子 2014年

![https://joelouismarino.github.io/images/blog_images/blog_googlenet_keras/googlenet_diagram.png](<https://joelouismarino.github.io/images/blog_images/blog_googlenet_keras/googlenet_diagram.png>)







## Average pooling + 1*1 Convolutions

- 这个将会优化上面介绍的金字塔式的卷积网络



## Inception Modules

- 这个也是google的最新技术，他们将会优化图像识别的技术



### AlphaGo Zero

深入了解了CNN之后，就可以理解AlphaGo Zero，简单的说就是MCTS+CNN，抛弃所有过去的经验，从而重新发现了人类历史上发现过的定式，还有就是对过去的定式进行了重新评估。

而之后的Alpha Zero（不同于AlphaGo Zero）更是泛化了这种算法，从而实现了在透明化棋局游戏内的泛化

#### 为何泛化很重要？

因为根据人类神经学的研究，人类发现动物其实是可以用听觉的器官去看世界的，也就是说人类大脑的本质上是以一种更简单的方式去处理很多物体。很多我们认为完全不同的事物和逻辑，其实本质上可能是一样内容。就像围棋上的各种定式，各种流派，各种棋风，其实换一个角度去看都可以用一个更简单的方式去解释。

#### DeepMind不是终点，CNN也不是，只是通往终点的过程

我们相信DeepMind，或者CNN、RNN、MCTS都不是终点，他们只是过程，是路径，通过他们我们将会用一个更简单，更美的方式去理解我们身边发生的很多事情，很多行业，和整个世界。



## 总结

CNN是目前的深度学习的一个热点，从上面的一些例子也可以看出，工程界在深入研究的过程中，不断优化和改进卷积网络，并提出了很多行之有效的改进措施



- 参考资料：
  - 机器学习-什么是卷积网络<https://www.youtube.com/watch?v=QsxKKyhYxFQ>
  - A guid to convolution arithmetic for deep learning. <https://arxiv.org/pdf/1603.07285v1.pdf>
  - 深度学习 （花书），Chapter 9 Page.201 
  - 优达学院-卷积分课程：<https://classroom.udacity.com/courses/ud730/lessons/6377263405/concepts/64063017560923>
  - Yann Lecun wiki：<https://zh.wikipedia.org/wiki/%E6%9D%A8%E7%AB%8B%E6%98%86>

  - Inception Modules: <https://hacktilldawn.com/2016/09/25/inception-modules-explained-and-implemented/>

  - Mastering the game of Go without human knowledge (Nature)

    <https://www.nature.com/articles/nature24270.epdf?author_access_token=VJXbVjaSHxFoctQQ4p2k4tRgN0jAjWel9jnR3ZoTv0PVW4gB86EEpGqTRDtpIz-2rmo8-KG06gqVobU5NSCFeHILHcVFUeMsbvwS-lxjqQGg98faovwjxeTUgZAUMnRQ>

  - AlphaGo Zero Nature围棋论文翻译 <https://cloud.tencent.com/developer/article/1087771>

  - A general reinforcement learning algorithm that masters chess, shoji, and Go through self-play (Science) <http://science.sciencemag.org/content/362/6419/1140>
  - 官网文章链接，个人更喜欢这个标题 AlphaZero: Shedding new light on the grand games of chess, shogi and Go <https://deepmind.com/blog/alphazero-shedding-new-light-grand-games-chess-shogi-and-go/>