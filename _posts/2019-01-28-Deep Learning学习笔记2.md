
# Deep Learning 学习笔记



- 多层神经网络

  - ReLU (rectified linear unit) 对所有负的输入返回0，所有X>0的输入，返回x

- 线性回归的参数问题

  - 如果一个图片是28*28，让你判断他是0-9里面的一个数字那么他总共给你更有多少个参数

    - 应该是 
      $$
      28 * 28 * 10 + 10 = 7850
      $$
      因为线性回归的公式是
      $$
      y = wx + b \\
      x = 28 * 28 \
      $$
      

  - 线性回归的局限性
    - 参数为 （N+1）K 
    - 比如上面的图片中像素为28*28，判断结果是0-9里面的一个数字。
    - 所以 $N = 28 * 28$, K = 10
    - 局限性就是这个N很可能会非常大

- 解决方式

  - 引入一个ReLU
  - ReLU是小于0的都返回0，大于0的返回y=x
  - 一个简单的2层神经网络
  - ![image-20190128061354457](https://ws2.sinaimg.cn/large/006tNc79gy1fzlvxjizvxj30ra0foacd.jpg)
  - 数学表示
  - ![image-20190128061501083](https://ws3.sinaimg.cn/large/006tNc79gy1fzlvyowlv6j315w0iz11r.jpg)



- 为什么可以这样做，是因为数学上的chain rule
  - ![image-20190128061645552](https://ws3.sinaimg.cn/large/006tNc79gy1fzlw0i6j71j30rh0i279t.jpg)