- 作者：

  - BigChen
- Step1: 在github上面开设一个repository
  - 设置repository的名字和自己的账号一样，比如
  - ![image-20190126190335301](https://ws2.sinaimg.cn/large/006tNc79gy1fzk7oiptk0j30av02jjrc.jpg)

- Step 2: 可以将这个repository 同步到本地

- Step 3: 搭建本地的jekyll环境，并设置主题

  - 搭建环境，见官网：<https://jekyllrb.com/docs/installation/>

  - 选择主题，推荐首先选择默认主题 **minima** 

    - 步骤详情：<https://github.com/jekyll/minima>

  - 首先在本地的文件夹下面执行

    ```
    jekyll new 
    然后在gem.file中配置 minima
    最后在_config.yml中配置theme
    ```

  - 这样一个最小本地环境就搭建好了。可以用 `jekyll serve` 来执行了



- 2019-01-26 补充

  - 如何将tensorflow的ipynb文件转化成markdown文件：

  - 来源：<https://blog.csdn.net/red_stone1/article/details/73380517>

  - ```
    jupyter nbconvert --to markdown notebook.ipynb
    ```

    