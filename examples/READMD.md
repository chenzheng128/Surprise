
### 我们的新增代码

* `benchmark_k.py` 参考 benchmark.py 使用不同的 k 值遍历实验 MAE 值，改变进行初始化, 修改相似度参数。

#### benchmark_k.py 100k  运行结果参考

benchmark_k.py 

consin 线性减小；

| [Movielens 100k](http://grouplens.org/datasets/movielens/100k)   |   RMSE |   MAE | Time    |
|:-----------------------------------------------------------------|-------:|------:|:--------|
| KNNBaseline@5                                                    |  1.042 | 0.821 | 0:00:28 |
| KNNBaseline@10                                                   |  0.989 | 0.78  | 0:00:27 |
| KNNBaseline@15                                                   |  0.968 | 0.763 | 0:00:27 |
| KNNBaseline@20                                                   |  0.957 | 0.754 | 0:00:28 |
| KNNBaseline@25                                                   |  0.951 | 0.75  | 0:00:29 |
| KNNBaseline@30                                                   |  0.946 | 0.746 | 0:00:31 |
| KNNBaseline@35                                                   |  0.943 | 0.744 | 0:00:32 |
| KNNBaseline@40                                                   |  0.942 | 0.742 | 0:00:33 |
| KNNBaseline@45                                                   |  0.94  | 0.741 | 0:00:34 |

benchmark_k.py pearson 一定值之后不变
| [Movielens 100k](http://grouplens.org/datasets/movielens/100k)   |   RMSE |   MAE | Time    |
|:-----------------------------------------------------------------|-------:|------:|:--------|
| KNNBaseline@5                                                    |  0.983 | 0.772 | 0:00:17 |
| KNNBaseline@10                                                   |  0.95  | 0.748 | 0:00:20 |
| KNNBaseline@15                                                   |  0.94  | 0.74  | 0:00:21 |
| KNNBaseline@20                                                   |  0.935 | 0.737 | 0:00:21 |
| KNNBaseline@25                                                   |  0.933 | 0.735 | 0:00:22 |
| KNNBaseline@30                                                   |  0.931 | 0.734 | 0:00:25 |
| KNNBaseline@35                                                   |  0.931 | 0.733 | 0:00:27 |
| KNNBaseline@40                                                   |  0.931 | 0.733 | 0:00:35 |
| KNNBaseline@45                                                   |  0.931 | 0.733 | 0:00:30 |

benchmark.py 原始结果

| [Movielens 100k](http://grouplens.org/datasets/movielens/100k)                                                                         |   RMSE |   MAE | Time    |
|:---------------------------------------------------------------------------------------------------------------------------------------|-------:|------:|:--------|
| [SVD](http://surprise.readthedocs.io/en/stable/matrix_factorization.html#surprise.prediction_algorithms.matrix_factorization.SVD)      |  0.936 | 0.738 | 0:00:29 |
| [SVD++](http://surprise.readthedocs.io/en/stable/matrix_factorization.html#surprise.prediction_algorithms.matrix_factorization.SVDpp)  |  ___0.922___ | 0.723 | 0:16:00 |
| [NMF](http://surprise.readthedocs.io/en/stable/matrix_factorization.html#surprise.prediction_algorithms.matrix_factorization.NMF)      |  0.964 | 0.758 | 0:00:27 |
| [Slope One](http://surprise.readthedocs.io/en/stable/slope_one.html#surprise.prediction_algorithms.slope_one.SlopeOne)                 |  0.946 | 0.743 | 0:00:20 |
| [k-NN](http://surprise.readthedocs.io/en/stable/knn_inspired.html#surprise.prediction_algorithms.knns.KNNBasic)                        |  0.98  | 0.774 | 0:00:19 |
| [Centered k-NN](http://surprise.readthedocs.io/en/stable/knn_inspired.html#surprise.prediction_algorithms.knns.KNNWithMeans)           |  0.951 | 0.749 | 0:00:21 |
| [k-NN Baseline](http://surprise.readthedocs.io/en/stable/knn_inspired.html#surprise.prediction_algorithms.knns.KNNBaseline)            |  ___0.931___ | 0.733 | 0:00:24 |
| [Co-Clustering](http://surprise.readthedocs.io/en/stable/co_clustering.html#surprise.prediction_algorithms.co_clustering.CoClustering) |  0.965 | 0.755 | 0:00:09 |
| [Baseline](http://surprise.readthedocs.io/en/stable/basic_algorithms.html#surprise.prediction_algorithms.baseline_only.BaselineOnly)   |  0.944 | 0.748 | 0:00:02 |
| [Random](http://surprise.readthedocs.io/en/stable/basic_algorithms.html#surprise.prediction_algorithms.random_pred.NormalPredictor)    |  1.523 | 1.222 | 0:00:02 |




### 参考示例代码

* 待补充
