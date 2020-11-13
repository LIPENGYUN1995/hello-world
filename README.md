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
