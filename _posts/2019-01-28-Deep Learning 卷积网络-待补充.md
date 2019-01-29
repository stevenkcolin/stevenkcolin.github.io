### 一些概念



#### stride 步数

- 如果input为 28 * 28， Conv = 1*1， stride = 1，就代表 
  $$
  conv(input) = 28 * 28
  $$

- 如果input = 27 * 27, conv = 3*3, stride = 1
  $$
  conv(input) = 9 * 9
  $$

- 如果input = 28 * 28 cone = 3*3，stride = 1
  - 这个时候有两个方式
  - Same Padding
    - 就是说要拿到和28*28一样的特征，也就是扩展为	30 * 30，最外面的由0补充即可
    - 那么得到的feature map就还是28 * 28
  - Valid Padding
    - 就是说不补充0，而需要满足3*3，那么实际上就会少掉一些信息。最终成为 26 * 26

#### Convolution 卷积

数学公式
$$
s(t) = (x * w) (t)
$$

- x = input
- w = kernel function
- 输出 = Feature Map = 特征映射



#### 

