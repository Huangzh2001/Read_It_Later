---
id: 31ff8470-df2c-4a12-a4be-c5a63c35ddc8

url: https://zhuanlan.zhihu.com/p/551134022
---


tags:: 

# Optimal Transport (OT) 最优传输-简介 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/optimal-transport-ot-19362777c98)
[Read Original](https://zhuanlan.zhihu.com/p/551134022)

---

## 1\. 概念（[蒙日问题](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%92%99%E6%97%A5%E9%97%AE%E9%A2%98&zhida%5Fsource=entity)）：  

蒙日（Monge）两百多前提出，将一个沙盘的沙子以最小花销传输到另外一个沙盘。另一种直观理解：把n个仓库的原料以最小代价传输到m个工厂。

## 2\. Kantorovich Relaxation（Kantorovich问题）：  

解除完全确定性传输的限制，允许同一点质量分解传输。基于此给出简洁最优传输模型，解耦合矩阵（Coupling Matrix）P来求解最优传输问题  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/726859950fcbd1ef4898a0c3acf08f3d_MD5.png]]

  
那么Kantorovich最优传输[问题定义](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E9%97%AE%E9%A2%98%E5%AE%9A%E4%B9%89&zhida%5Fsource=entity)为  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/81e6010a120ec49d3fdf437ee4e725f3_MD5.png]]

## 3\. 例子，对于离散[概率向量](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E6%A6%82%E7%8E%87%E5%90%91%E9%87%8F&zhida%5Fsource=entity)（直方图）  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/f2fb6c8de5736a3e68fa18a00c94d926_MD5.png]]

  
[耦合矩阵](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=2&q=%E8%80%A6%E5%90%88%E7%9F%A9%E9%98%B5&zhida%5Fsource=entity)P表示的传输过程如下  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/7ab2b1eb47fadba0a8e3f44dc3f9a474_MD5.jpg]]

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/39a430ddee9c8d10de7c1fef14b381d6_MD5.jpg]]

## 4\. Wasserstein Distance：

  
对Kantorovich最优传输问题，假设n=m，对某些p≥1，[代价矩阵](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E4%BB%A3%E4%BB%B7%E7%9F%A9%E9%98%B5&zhida%5Fsource=entity) C\=Dp\=(Dijp)ij∈Rn×nC=D^p=(D\_{ij}^p)\_{ij}∈R^{n×n} ，其中 D∈R+n×nD∈R\_+^{n×n} 为对称[距离矩阵](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%B7%9D%E7%A6%BB%E7%9F%A9%E9%98%B5&zhida%5Fsource=entity)，那么距离定义为  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/5c5ecd4a9c100b41b66f7fde7b435a5b_MD5.png]]

  
即  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/368343a170bcbf220a75e0445b6c69d6_MD5.png]]

  
**对Wasserstein距离的一种不全面理解**:

对两个分布a, b,给定各点对的距离(花销),求解一个类Kantorovich OT问题,最优[联合概率](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%81%94%E5%90%88%E6%A6%82%E7%8E%87&zhida%5Fsource=entity)P可使得两分布的距离最小(即使以概率P加权的距离求和最小),这个最小距离称为Wasserstein距离,这是一种链接几何与概率来衡量两个分布距离的方式

## 5\. 熵(Entropic)正则化:   

Kantorovich最优传输问题是一个特殊的[线性规划](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E7%BA%BF%E6%80%A7%E8%A7%84%E5%88%92&zhida%5Fsource=entity)问题，所以先进的线性规划求解算法均可用来进行求解。然而当面对大规模问题时，基于[内点法](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E5%86%85%E7%82%B9%E6%B3%95&zhida%5Fsource=entity)的线性规划算法依然有较大的局限性, 若利用[正则化](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=2&q=%E6%AD%A3%E5%88%99%E5%8C%96&zhida%5Fsource=entity)，改求近似解，那么可大幅减少最优传输的计算代价  
定义正则化项为  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/cdb7d699cf8c5a0a47c2b4bae5ede9d3_MD5.png]]

  
那么[熵正则化](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E7%86%B5%E6%AD%A3%E5%88%99%E5%8C%96&zhida%5Fsource=entity)的Kantorovich问题可表示为  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/d4c8c27c5dccae8b1f369c0760000394_MD5.png]]

  
∈为[正则化系数](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E6%AD%A3%E5%88%99%E5%8C%96%E7%B3%BB%E6%95%B0&zhida%5Fsource=entity),其影响如下图,值越大最优解P的耦合程度越稀疏,可降低计算复杂度;反之值越趋近于0越收敛于Kantorovich问题的最优解  

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/f868e42357da7838f59072ecab25c7aa_MD5.png]]

## 6\. Sinkhorn算法:

熵正则化的Kantorovich问题的对偶问题的解满足

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/bb29cd983481aa2034b6fcfd2de49bc1_MD5.png]]

即解P是K经由u和v的一种映射。那么给定K,[迭代求解](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%BF%AD%E4%BB%A3%E6%B1%82%E8%A7%A3&zhida%5Fsource=entity)映射u和v即可求解P。

由最有传输的[质量守恒条件](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%B4%A8%E9%87%8F%E5%AE%88%E6%81%92%E6%9D%A1%E4%BB%B6&zhida%5Fsource=entity),可知a, b和u, v满足

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/31918ff36fecc8ad925d2afef4ffcf29_MD5.png]]

也即

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/9d54eb795b361252b9e6b3de8c36dc26_MD5.png]]

那么,可经过如下[迭代策略](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=1&q=%E8%BF%AD%E4%BB%A3%E7%AD%96%E7%95%A5&zhida%5Fsource=entity)求解u和v,进而求解P

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/bafc5192938a122f108faabb544f3adb_MD5.png]]

[Sinkhorn算法](https://zhida.zhihu.com/search?content%5Fid=210606807&content%5Ftype=Article&match%5Forder=2&q=Sinkhorn%E7%AE%97%E6%B3%95&zhida%5Fsource=entity)等价于求解问题的对偶问题的交替梯度上升方法,求解的是近似的Kantorovich最优传输问题，越小的∈可以获得越精确的近似，但是较小的∈会导致Sinkhorn算法的数值不稳定性

## 7\. 应用:

* WGAN

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/9ffe6c0b6caa16d936d74c69f129b6fa_MD5.png]]

* 零样本学习

![[Omnivore/Optimal Transport (OT) 最优传输-简介 - 知乎/attachments/35c945e4676d3a0dc3ac842edbae4feb_MD5.png]]

## 8\. 引用

[祥丰：计算最优传输（Computational Optimal Transport）](https://zhuanlan.zhihu.com/p/94978686)

[运筹千里纵横论坛｜王祥丰：计算最优传输及其应用浅谈\_哔哩哔哩\_bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1Gf4y1q74x%3Fvd%5Fsource%3D19249d865f30b6d773b0950b2862daac)

[最优运输（Optimal Transfort）：从理论到填补的应用](https://link.zhihu.com/?target=https%3A//www.cnblogs.com/liuzhen1995/p/14524932.html)

### 内容所属专栏

