# hello-world
ideas, resources
Hi guys!

LI here. I am studing economics and gender studies in Japan as an international student.
I am interested in everything I haven't heard before, so I start learning coding from now on!

1. variables 変数　（input varianbles + output variables）
Y=f(X)+ε εはrandom error, independent of X.
1.1 估计f的目的 1⃣️prediction 予測　　只要预测准就行，不关心模型形式 Reducible error（f）・Irreducible error(ε) 目標：Reducible errorを減らす 2⃣️Inference 推論　　关心模型形式。那些predictor和response有关，什么关系，是否能用线性模型（linear models）解释。
1.2 怎么估计f 1⃣️Parametric Methods 参数估计 假设f形状（形式）eg线性模型，用training data去fit模型 将估计f变成估计参数（贝塔123，，，）问题是对模型估计不够准确。选择flexible模型会更精确但可能overfitting（过度拟合）2⃣️Non-parametric Methods 非参数方法 不假设f的form，直接训练模型。能提高准确性但需要更多training data。
1.3 The Trade-Off Between Prediction Accuracy and Model Interpretability（解释性）flexible（或者说是预测准确性）和interpretability不可兼得（eg最小二乘法不太flexible但很好解释） flexibility=prediction accuracy
1.4 Supervised（监督） Versus Unsupervised Learning 监督是xy间的关系 非监督是各种x间的关系
1.5
2. 评估模型准确性 根据数据set选择合适的统计方法 2.1 测量fit的质量 mean squared error（MSE）均方误差MSE = 1/n＊総和(yi − f^(xi))2,  test MSE越小越好！ The degrees of freedom is a quantity that summarizes the flexibility of a curve.  The degrees of freedom大きくなると、training MSE小さくなる、test MSE（重要） U型。overfittingはtraining MSE小さく、test MSE大きい。　　cross-validation is a method for estimating test MSE using the training data.
2.2 The Bias-Variance Trade-Off(Bias-Variance的平衡)  E (y0 − f^(x0))2 = Var(f^(x0)) + [Bias(f^(x0))]2 + Var(ε). (2.7)即期待MSE由三种“误差”组成.  more flexible statistical methods have higher variance/more flexible methods result in less bias.  as we use more flexible methods, the variance will increase and the bias will decrease. 
2.3 The Classification Setting（分类的情况） error rate=1/n1到n总和I(y0不等于yˆ0）（2.8）  indicator variable指示变量  test error=Ave(I(y0不等于yˆ0))（2.9），A good classifier is one for which the test error is smallest.     1⃣️The Bayes Classifier conditional probability条件概率:Pr(𝑌=𝑗 | 𝑋=𝑥0)(2.10) Bayes decision boundary. 基于predictor值，将每一个observation推测为最有可能的class。即使得 Pr(𝑌=𝑗 | 𝑋=𝑥0)这个概率最大。例如，在binary classification问题上，如果 Pr(𝑌=1 | 𝑋=𝑥0)>0.5,则预测class one，否则预测class two。Bayes Classifier 可以产生 lowest possible test error rate, Bayes error rate: 1−𝐸(max𝑗Pr(𝑌=𝑗|𝑋))      2⃣️K-Nearest Neighbors  在现实中，由于无法得知在 𝑋条件下𝑌的分布，所以无法计算Bayes Classifier。而KNN classifier 是一个很接近Bayes Classifier的方法。Pr(𝑌=𝑗 | 𝑋=𝑥0)=1/𝐾∑𝑖∈𝑁0𝐼(𝑦𝑖=𝑗)。KNN Classifier 和 Bayes Classifier的接近程度部分取决于K的选择，K越小，flexibility越大，反之越小。和回归情况一样，当K=1时会overfitting，training error rate等于0，但test error rate很高。 test error和training error随flexible的增加变化趋势跟test MSE和training MSE趋势一样（U型和一直下降）


