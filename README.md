# machine_learning
哈尔滨工业大学2018年秋季机器学习相关实验

## Update：

在正心自习的时候，偶然看到前面的同学在看这个里面的实验报告复习，让我很担心我里面写的小错误会影响他们的考试。。。

请以后看这个仓库的同学，如果发现错误及时PR，**另外我的水平真的非常非常有限，请参考老师PPT、李航博士的《统计机器学习》、周志华老师的《机器学习》和Bishop的PRML来复习！**

另外，发现里面公式的输入也有问题，好多不够规范，比如`argmin`的写法，就请参考[Command for argmin or argmax?](https://tex.stackexchange.com/questions/5223/command-for-argmin-or-argmax)，当时处在刚学习LaTeX没多久的情况，很多符号都是看着像什么就打的什么:new_moon_with_face::new_moon_with_face:。

----

这个仓库用于对2018年秋季哈工大机器学习相关实验的备份。对于这个学期的ML课程，在考试结束后的一天对课程内容进行一些总结。

总的来说这门课程是大学以来最**硬核**的一门课程。虽然这只是机器学习入门的非常基础的知识，但是这种利用数学工具以及对数学背后的物理含义的更深理解，是这门课给我留下的最深印象；在考前复习的时候，对很多上课时提到的问题重新梳理，有了更清晰的理解。希望以后可以继续学习相关的知识，也推荐给后来的同学这门课程。

~~但是真的考炸了啊，虽然实验没炸。~~

## 仓库组成
- 实验代码 lab1~lab4
- [课程使用的PPT](https://github.com/1160300314/machine_learning/tree/master/PPT)
- [参考的cmu考试题目](https://github.com/1160300314/machine_learning/tree/master/exam_cmu)
- [复习机器学习的笔记](https://github.com/1160300314/machine_learning/blob/master/%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E5%A4%8D%E4%B9%A0%E7%AC%94%E8%AE%B0.pdf)

## lab 1 多项式拟合正弦函数
- [x] 1. 生成数据，加入噪声；
- [x] 2. 用高阶多项式函数拟合曲线；
- [x] 3. 用解析解求解两种loss的最优解（无正则项和有正则项）
- [x] 4. 优化方法求解最优解（梯度下降，共轭梯度）；
- [x] 5. 用你得到的实验数据，解释过拟合。
- [x] 6. 用不同数据量，不同超参数，不同的多项式阶数，比较实验效果。
- [x] 7. 语言不限，可以用matlab，python。求解解析解时可以利用现成的矩阵求逆。梯度下降，共轭梯度要求自己求梯度，迭代优化自己写。不许用现成的平台，例如pytorch，tensorflow的自动微分工具。

## lab 2 Logistics Regression 逻辑回归
- [x] 1.实现两种损失函数的参数估计（1、无惩罚项；2、加入对参数的惩罚），可以采用梯度下降、共轭梯度或者牛顿法等。

- [x] 2. 可以手工生成两个分别类数据（可以用高斯分布），验证你的算法。考察类条件分布不满足朴素贝叶斯假设，会得到什么样的结果。
- [x] 3. 逻辑回归有广泛的用处，例如广告预测。可以到UCI的网站上，找一实际数据加以测试，共使用3种不同数据(Mushroom, Blood Donation 和Banknote)。

## lab 3 实现k-means聚类方法和混合高斯模型
### 实验目标
- [x] 实现一个k-means算法和混合高斯模型，并用EM算法估计模型中的参数。
### 测试
用高斯分布产生k个高斯分布的数据(不同均值和方差)(其中参数自己设定)
- [x] 用k-means聚类测试效果
- [x] 用混合高斯模型和你实现的EM算法估计参数，看看每次迭代后似然值变化情况，考察EM算法是否可以获得正确结果(与你的设定结果比较)。
### 应用
- [x] 可以在UCI上找一个简单数据，用你实现的GMM进行聚类。
<!-- 存在问题 在Iris数据上GMM表现一般 -->

## lab 4 PCA模型实验
### 实验目标
实现一个PCA模型，能够对给定数据进行降维(即找到其中的主成分)，可以利用已有的矩阵特征向量提取方法。
### 测试
- [x] 首先人工生成一些数据（如三维数据），让它们主要分布在低维空间中，如首先让某个维度的方差远小于其它维度，然后对这些数据旋转。生成这些数据后，用你的PCA方法进行主成分提取。
- [x] 利用手写体数字数据mnist，用你实现PCA方法对该数据降维，找出一些主成分，然后用这些主成分对每一副图像进行重建，比较一些它们与原图像有多大差别（可以用信噪比衡量）。
