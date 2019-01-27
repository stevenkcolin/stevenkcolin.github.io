- 作者：stevenkcolin

  # 深度学习围棋Leela Zero和区块链随想

  ### Leela Zero介绍

  - Leela Zero是一个外国程序员根据DeepMind的论文所开发的人工智能围棋程序，
  - 借助于大家共同帮忙计算的算力从而不断训练他的神经网络，从而使得leela zero可以被平民使用
  - 具体介绍大家可以去leela zero的官网和github地址去看
    - <https://github.com/gcp/leela-zero>
    - 中文网站：<https://hhpetra.github.io/leelachinese/>

  ##### 安装步骤

  - 分为两部分，开发和编译Leela，还有就是启动他的UI程序：lizzie

  - 开发和编译Leela - mac版本

    - ```
      	### Example of compiling Leela Zero - macOS ###
        		# Clone github repo
        		git clone https://github.com/gcp/leela-zero
        		cd leela-zero/src
        		brew install boost
        
        		## OPTIONAL: if you want to compile the CPU-only version of Leela Zero, open config.h and replace the line
        		##     #define USE_OPENCL
        		## with
        		##     //#define USE_OPENCL
        
        		# Compile Leela Zero
        		make
      ```

      

    - 编译出来Leela

    - ![image-20190127145528641](https://ws3.sinaimg.cn/large/006tNc79gy1fzl5dx1axpj30cd00wjrf.jpg)

    - 那就把他copy到lizzie的目录下去

      - lizzie的github地址

        - <https://github.com/featurecat/lizzie>

      - lizzie有release版本，可以直接下载。

      - 当leela在lizzie文件夹下面的时候，那么就可以直接双击，或者用下面命令即可

      - ```
        java -jar "lizzie.jar" 
        ```

  - 好的完成上面步骤之后，启动界面如图所示：

  - ![image-20190127145841408](https://ws3.sinaimg.cn/large/006tNc79gy1fzl5hddtmhj30sg0lc4qp.jpg)



### 打开这个之后就可以食用了，当然我们也可以装别的客户端来打开leela,比如sabazuki等等



- 通过这个软件，我打开了两盘之前alpha go 和 alpha lee的棋局，配合上一个挺喜欢的棋局解说，看到了很多之前没有注意到的。
  - 结束连接：<https://www.youtube.com/watch?v=m13QHNMHAa4>



- 第一：因为可以看出每一步棋局的胜率，可以看到在平等对弈的开始，到天平向一方倾斜。很多时候就是一步棋走错，天平于是就开始倾斜，胜率一旦超过了70这个不平衡线后，基本上就很难翻盘了。



- 第二：从微信团队开发的“金毛”（现在改名为phoenixGo）围棋，打败老版本的绝艺上来看（新闻链接：http://www.sohu.com/a/229909714_473283）
  以及之后Leela这个开源项目打败众多AI，仅输给腾讯的两款游戏上面来看，算法/数学/认知模式上的提升才是最最关键的，如果选错了方法，那么投入的时间和精力不过是为了给后来者证明**此路不通**

  而之后的新一代Zero类围棋（典型代表 Phoenix Go 和Leela Zero），基本都采用了DeepMind的论文算法，而他们的实力之间的差距也基本上可以认为主要就是在计算力上。

  

  **如果没有数学的底层改进，那么算力之间的竞争，或者是工程方面的改进，其实就变成了一个很无趣的游戏了**



- 第三：接上面的，感谢DeepMind团队，无论是CEO还是DeepMind项目核心 David Silver。他们简单明了的算法，就和比特币一样，给人类打开了一扇门，一扇重新认识我们整个世界的大门，很多事情并不像我们过去所认为的那样复杂，只要找到了正确的道路，我们就能迎来我们所期望的指数级增长。

  最典型的就是Alpha系列了，基本上AlphaGo Zero甚至更新的AlphaZero 碾压当时战胜李世石的版本，基本上就是指数级的碾压。

- 第四：因为围棋是一个充分信息透明的游戏，而在这个游戏里面，机器已经展示了他们的认知和机会的把握能力的确远远超过人类。那么在信息不透明的游戏中呢？事实上只要进行适当的对信息不透明进行处理，电脑一样可以展现出超越人类的处理水平
  	新闻链接：“阿尔法星际”正式亮相 10比0人类职业选手 http://sports.sina.com.cn/go/2019-01-25/doc-ihqfskcp0200300.shtml



#### 第五: Leela这个比利时工程师，因为需要的算力没有办法自己完成，但是他通过网络和开源社区，得到了大家的支持，也已经在18年9月份成功达到了Block40的水平，但最大的瓶颈却是资源，不论是计算资源，还是存储资源，当然还有就是负责人自己是否有意愿去直面这些大象的竞争（无论腾讯的phoenix，facebook的ELF OpenGo都是大象）

（链接：<https://zh.wikipedia.org/wiki/Leela_Zero>）



## 也许：如此优秀的项目缺少的恰恰就是一个通证，从而将人和资源粘合在一起（而且是全球的）





