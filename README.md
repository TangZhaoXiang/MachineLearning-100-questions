# 机器学习面试题汇总

内容基本上来源于网络，由TangZhaoXiang整理汇集排版，总结于2019.10.8，目前150多页涵盖最常见的**过拟合、最优化方法、特征工程、SVM、决策树、朴素贝叶斯、逻辑回归、XGBoost、GBDT、随机森林、Adaboost等**高频考题



![img](http://imagecn.gasgoo.com/moblogo/News/UEditor/image/20170804/6363745574453364348223382.jpg)



**目录**

## 一、 机器学习基础	1

1. 请简要说说一个完整机器学习项目的流程	2   
2.简单说下有监督学习和无监督学习的区别	2  
3.线性分类器与非线性分类器的区别以及优劣	3  
增：特征比数据量还大时，选择什么样的分类器？	3  
4. 对于维度很高的特征你选择线性分类器还是非线性分类器？维度很低的特征又该如何选择？	3  
5.什么是生成模型和判别模型?	3  
增：生成方法和判别方法的优缺点	4  
6.常见的生成式模型和判别式模型有哪些？ 	4  
7.解释置信区间	4  
8. 什么是过拟合？	4  
9.什么是正则化?	5  
10.什么是L1正则化和L2正则化？	5  
11.为什么L1正则化相较于L2正则化会产生更加稀疏的矩阵？	5  
增：L1范数和L2范数的区别	5  
增：L1和L2正则先验分别服从什么分布 ？	6  
增：机器学习中L1正则化和L2正则化的区别是？（AD）	6  
12. 正则化为什么能防止过拟合？\*	6  
13.机器学习中经常使用的最优化方法有哪些？	6  
14.简述一下梯度下降法	9  
增：梯度下降法找到的一定是下降最快的方向么？	9  
增：关于牛顿法和梯度下降法的效率对比	9  
增：请说说随机梯度下降法的问题和挑战？	10  
15.如何处理样本不均衡问题？	10  
16.如何衡量分类器的好坏？\*	10  
17.介绍一下ROC和AUC*	11  
*18.为什么要使用ROC曲线？	11  
19.什么是交叉验证？	11  
20、简述交叉验证常见的几种方法	12  
增：偏差和方差	13  

## 二、 特征工程相关	16
1.什么是特征工程？	17  
*2.对于一个新的项目如何生成模型所需要使用的特征？	17  
3.原始数据通常存在哪些问题？	17  
4.谈谈你所了解的数据抽样方法	17  
5.什么是归一化？为什么一些机器学习模型需要对数据进行归一化？	17  
6.常用的归一化方法有哪些？	18  
7.归一化为什么能提高梯度下降法求解最优解的速度？	18  
8.归一化有可能提高精度吗？	19  
9.哪些机器学习算法不需要做归一化处理？	19  
10.对于树形结构为什么不需要归一化？	19  
11.什么是数据中的异常值，如何发现数据中的异常值？	20  
12.数据中的异常值如何处理？	21  
13. 原始数据中缺失值处理方式	22  
14.什么是特征选择，为什么要进行特征选择？	23  
15.特征选择有哪些方法？	23  
16.如何使用卡方检验进行特征选择？	23  
17.什么是特征提取，它与特征选择有什么区别？	23  
增：什么是特征构建？	24  
18.简述主成分分析PCA工作原理	24  
*19.PCA会有第一主成分、第二主成分，他们是怎么确定的？为什么第一主成分是第一，原因是什么？	26  
20、 PCA的优缺点有哪些？	26  
增：正负样本不平衡处理办法	26  

## 三、 决策树相关	29
1. 简述决策树的原理	30  
2.简述决策树的构建过程	30  
3.信息增益率有什么优缺点？	31  
增：信息增益做特征选择的优缺点	32  
4.如何对决策树进行剪枝？	32  
5.为什么决策树需要进行剪枝?	33  
6.C4.5对ID3做了哪些改进？	34  
7.C4.5决策树算法如何处理连续数值型属性？	36  
8.C4.5与CART的区别	36  
\*9.简述一下分类树和回归树	37  
增：如何建立回归树	38  
10.CART如何生成回归树？	38  
11.CART树对离散特征取值数目>=3的特征如何处理？	38  
12.决策树对缺失值如何处理？	39  
13.如果决策树属性用完了仍未对决策树完成划分应该怎么办？	40  
14.如何避免决策树的过拟合？	40  
15.决策树需要进行归一化处理吗？	40  
16.常用的决策树一定是二叉树吗？二叉决策树与多分支决策树相比各有什么特点？	40  
17.你认为在一棵决策树构建过程中较为耗时的步骤是什么？	41  
\*18.你正在一个时间序列数据集上工作，开始用决策树算法，因为你知道它在所有类型数据上的表现都不错。后来，你尝试了时间序列回归模型，并得到了比决策树模型更高的精度。这种情况会发生吗？为什么？ 	41  
19.决策树在选择特征进行分类时一个特征被选择过后，之后还会选择到这个特征吗？	41  
20.和其他模型比，决策树有哪些优点和缺点？	41  
增：树模型的应用场景	42  

## 四、逻辑斯蒂回归相关	44
1.逻辑斯蒂回归推导	45  
增：逻辑回归的基本假设	46  
增：逻辑回归如何分类	47  
\*2.简述一下线性回归	47  
3.为什么逻辑斯特回归中使用最大似然函数求得的参数是最优可能的参数值？	47  
4.逻辑回归是线性模型吗？	47  
5.逻辑回归做分类的样本应该满足什么分布？	47  
6.逻辑回归输出的值是0到1之间的值，这个值是真实的概率吗？	47  
7.逻辑回归与线性回归的联系和区别？	48  
8.逻辑回归会发生过拟合吗？如何解决？	49  
9.什么是特征离散化和特征交叉？	49  
10.逻辑斯特回归为什么要对特征进行离散化？	49  
11.在逻辑回归模型中，为什么常常要做特征组合（特征交叉）？	49  
12.逻辑回归在训练的过程当中，如果有很多的特征高度相关或者说有一个特征重复了100遍，会造成怎样的影响？	49  
13.为什么逻辑回归在训练的过程当中将高度相关的特征去掉？	50  
14.逻辑回归最优化过程中如何避免局部极小值？	50  
15. 线性回归的损失函数里面为什么常用平方形式, 而不是1次方，3次方，4次方或者绝对值？	50  
16.逻辑回归特征系数的绝对值可以认为是特征的重要性吗？	50  
17.如何使用逻辑回归实现多分类？	50  
18.逻辑回归的损失函数为什么要使用极大似然函数作为损失函数？	51  
19.逻辑回归参数归一化是否对结果有什么影响吗？	51  
20.逻辑回归有哪些优缺点	52  

## 五、贝叶斯相关	54
1.简述朴素贝叶斯算法原理和工作流程	55  
2.什么是先验概率和后验概率？	56  
3.什么是条件概率？	56  
增：为什么要后验概率最大化：	57  
4.为什么朴素贝叶斯如此“朴素”？	57  
5.什么是贝叶斯决策理论？	57  
6.朴素贝叶斯算法的前提假设是什么？	59  
7.为什么属性独立性假设在实际情况中很难成立，但朴素贝叶斯仍能取得较好的效果?	60  
8.朴素贝叶斯可以做多分类吗？	61  
增：朴素贝叶斯中有没有超参数可以调？	61  
9.什么是朴素贝叶斯中的零概率问题？如何解决？	62  
10.朴素贝叶斯中概率计算的下溢问题如何解决？	62  
11.朴素贝叶斯分类器对异常值敏感吗?	62  
12.当数据的属性是连续型变量时，朴素贝叶斯算法如何处理？	63  
13.朴素贝叶斯算法对缺失值敏感吗？	63  
14.朴素贝叶斯有哪几种常用的分类模型？	63  
15.朴素贝叶斯算法中使用拉普拉斯平滑，拉普拉斯因子的大小如何确定？	63  
16.为什么说朴素贝叶斯是高偏差低方差？	64  
17.朴素贝叶斯什么时候增量计算？	64  
18.高度相关的特征对朴素贝叶斯有什么影响？	64  
19.朴素贝叶斯的应用场景有哪些？	64  
20.朴素贝叶斯有什么优缺点？	64  
增：朴素贝叶斯与LR的区别？	65  
增：极大似然估计和贝叶斯估计	66  
增：朴素贝叶斯例题	67  
增：网页搜索中的拼写检查可以基于贝叶斯实现，你怎么理解？	68  

## 六、 K-means，KNN相关	69
1.简述一下K-means算法的原理和工作流程	69  
2.简述一下KNN算法的原理	70  
3.KNN算法有哪些优点和缺点？	70  
4.不平衡的样本可以给KNN的预测结果造成哪些问题，有没有什么好的解决方式？	71  
5.为了解决KNN算法计算量过大的问题，可以使用分组的方式进行计算，简述一下该方式的原理。	71  
6.什么是欧氏距离和曼哈顿距离？	71  
增：为什么用欧式不用曼哈顿？	72  
7.KNN中的K如何选取的？	73  
8.什么是KD树？	73  
9.KD树建立过程中切分维度的顺序是否可以优化？	74  
10.KD树每一次继续切分都要计算该子区间在需切分维度上的中值，计算量很大,有什么方法可以对其进行优化？	74  
11.K-means中常用的到中心距离的度量有哪些？	74  
12.K-means中的k值如何选取?	75  
13.K-means算法中初始点的选择对最终结果有影响吗？	76  
14.K-means聚类中每个类别中心的初始点如何选择？	76  
15.K-means中空聚类的处理	76  
增：初始的K个质心怎么选？	76  
16.K-means是否会一直陷入选择质心的循环停不下来？	76  
17.如何快速收敛数据量超大的K-means？	76  
18.K-means算法的优点和缺点是什么？	77  
\*19.如何对K-means聚类效果进行评估？	78  
20.K-Means与KNN有什么区别	78  

## 七、 支持向量机相关	80
增：线性不可分和非线性问题区别	81  
1.SVM的原理是什么？	81  
2.SVM推导	82  
增：函数间隔和几何间隔	82  
3.简述SVM软间隔	84  
4.如何使用SMO最优化方法求解SVM模型？	84  
\*5.SMO算法中对于每次选中的α如何进行优化？	85  
6.SMO算法中如何选择每次优化的两个α？	85  
\*7.SMO算法优化的终止条件是什么？	86  
8.什么是核函数，为什么SVM要引入核函数？	86  
9.SVM常用的核函数有哪些，如何选择核函数？	88  
10.为什么要将求解SVM的原始问题转换为其对偶问题？	89  
11.SVM为什么采用间隔最大化？	89  
\*12.SVM对噪声敏感的原因	89  
13.为什么SVM对缺失某些特征数据敏感？	90  
14.SVM的优缺点 	90  
15.SVM为什么用在大数据有哪些缺陷？	91  
16.如何防止SVM过拟合（提高泛化能力）？	91  
17.SVM如何调节惩罚因子C?	92  
18.如何处理SVM中样本不平衡的问题？	92  
19.支持向量机(SVM)中的支持向量是什么意思?	93  
20.SVM如何处理多分类问题？	93  
增：SVM和感知机的区别？	94  
增：SVM如何处理线性不可分的问题	94  

## 八、集成学习相关（一）	97
1.什么是集成学习算法？	98  
2.集成学习主要有哪几种框架？	98  
3.简单介绍一下bagging，常用bagging算法有哪些？	98  
4.简单介绍一下boosting，常用boosting算法有哪些？	99  
5.boosting思想的数学表达式是什么？	100  
6.简单介绍一下stacking，常用stacking算法有哪些？	100  
7.你意识到你的模型受到低偏差和高方差问题的困扰，应该使用哪种算法来解决问题呢？为什么？	101  
8.简述一下随机森林算法的原理	102  
增：随机森林的生成过程	102  
9.随机森林的随机性体现在哪里？	103  
增：随机森林分类效果的影响因素	103  
10.随机森林为什么不容易过拟合？	103  
11.你已经建了一个有10000棵树的随机森林模型。在得到0.00的训练误差后，你非常高兴。但是，验证错误是34.23。到底是怎么回事？你还没有训练好你的模型吗？	104  
增：什么是OOB？随机森林中OOB是如何计算的，它有什么优缺点？	104  
12.如何使用随机森林去弥补特征向量中的缺失值	104  
13.如何使用随机森林对特征重要性进行评估？	105  
14.随机森林算法训练时主要需要调整哪些参数？	105  
15.随机森林为什么不能用全样本去训练m棵决策树？	105  
16.随机森林算法有哪些优缺点	106  
17.简述一下Adaboost原理	106  
18.AdaBoost的优点和缺点	107  
19.为什么Adaboost对噪声敏感？	108  
增：Adaboost的自适应在于？	108  
20.Adaboost和随机森林算法的异同点	108  
增：提升树与残差	108  
增：一个GDBT的示例	109  

## 八、 集成学习相关（二）	112
1.简述GBDT原理	113  
增：Adaboost和GBDT的区别？	114  
2.GBDT常用损失函数有哪些？	114  
3.GBDT中为什么要用负梯度来代替残差计算？	116  
4.GBDT如何用于分类?	116  
5.GBDT中的决策树是分类树还是回归树？	116  
6.如何使用GBDT构建特征？	116  
7.为什么GBDT不适合使用高维稀疏特征?	116  
8.GBDT通过什么方式减少误差？	117  
9.GBDT如何进行正则化？ 	117  
10.GBDT里的G代表什么，体现在哪里？	117  
11.GBDT需要调试的参数有哪些？	118  
12.GBDT算法的优缺点有哪些？	118  
增：简述Xgboost原理	118  
13.Xgboost/GBDT在调参时为什么树的深度很少就能达到很高的精度，而随机森林需要的深度相对较高？	119  
14.为什么Xgboost要用泰勒展开，优势在哪里？	120  
15.Xgboost如何寻找最优特征？	121  
16.Xgboost采样是有放回还是无放回的呢？	121  
17.XGBoost训练通常调整的参数有哪些？	121  
18.XGBoost中的树是如何剪枝？	121  
19.XGBoost如何解决缺失值问题？	121  
增：XGBoost如何防止过拟合？	122  
增：XGBoost的优点	122  
20.XGBoost和GBDT的区别	122  
增：XGBoost比GBDT的改进点？	123  
增：GBDT与提升树的区别	124  

## 九、其它	126
1.把我当成一个5岁的小孩来解释机器学习	126  
2.什么是DBSCAN	126  
3.LDA的原理	126  

## 十、算法推导	128
1.朴素贝叶斯算法	128  
2.KNN算法	129  
3.CART回归树算法	130  
4.SVM—最大间隔法	131  
5.SVM—对偶解法	132  
6.SMO算法	135  
7.Adaboost算法	136  
8.GBDT算法	137  
9.Xgboost算法	138  
