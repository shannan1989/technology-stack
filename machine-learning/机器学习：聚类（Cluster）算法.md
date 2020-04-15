下面介绍一下机器学习中几种常用的聚类算法。

## K-Means（K均值算法）

## Mean-Shift（均值迁移算法）

### 基本思想

在数据集中选定一个点，然后以这个点为圆心，r为半径，画一个圆（二维下是圆），求出这个点到所有点的向量的平均值，而圆心与向量均值的和为新的圆心，然后迭代此过程，直到满足一点的条件结束。（Fukunage在1975年提出）

### 图解过程

用下面几张图来说明Mean-Shift的基本过程。

![](./image/cluster-mean-shift.png)

由上图可以很容易看到，Mean-Shift 算法的核心思想就是不断的寻找新的圆心坐标，直到密度最大的区域。

### 算法函数

- 核心函数：sklearn.cluster.MeanShift（核函数：RBF核函数）

    圆心(或种子)的确定和半径(或带宽)的选择，是影响算法效率的两个主要因素。

    所以在sklearn.cluster.MeanShift中重点说明了这两个参数的设定问题。

- 主要参数

    bandwidth：半径(或带宽)，float型。如果没有给出，则使用 sklearn.cluster.estimate_bandwidth 计算出半径(带宽)。（可选）

    seeds：圆心（或种子），数组类型，即初始化的圆心。（可选）

    bin_seeding：布尔值。如果为真，初始内核位置不是所有点的位置，而是点的离散版本的位置，其中点被分类到其粗糙度对应于带宽的网格上。将此选项设置为True将加速算法，因为较少的种子将被初始化。默认值：False。如果种子参数(seeds)不为None，则忽略。

- 主要属性

    cluster_centers_：数组类型。计算出的聚类中心的坐标。

    labels_：数组类型。每个数据点的分类标签。

## Spectral Clustering（谱聚类算法）

## Hierarchical Clustering（层次聚类算法）

## DBSCAN（Density-Based Spatial Clustering of Applications with Noise，具有噪声的基于密度的聚类算法）

## Birch
