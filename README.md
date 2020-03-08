# 一、front-end 前台相关  
## 1.1 流程参考  
1. [h2o流程参考](https://h2oai.github.io/tutorials/machine-learning-experiment-scoring-and-analysis-tutorial-financial-focus/#0)
2. 
## 1.2 技术/包参考 
1. [vue-stepper](https://github.com/PygmySlowLoris/vue-stepper)
2. [vue-stepper-component](https://github.com/adi518/vue-stepper-component)
3. 
## 1.3 可视化与前台的交互
1. 传数据，前台处理展示  
2. 找python交互库  [比如](https://towardsdatascience.com/how-to-write-web-apps-using-simple-python-for-data-scientists-a227a1a01582)  
3. python 封装好函数，自动生成一系列图表，返回图表到前端，前端直接展示（简单，没交互感）  
4. 参考NNI的实现：tsx
[可以结合VUE](https://www.zhihu.com/question/281812349?sort=created)  
【至于tsx,一般情况用的不多,在少量的交互逻辑特别重但视图简单的组件中有使用,一般情况感觉没必要用tsx】

# 二、back-end 后台相关
## 2.1 特征工程参考
1. Featuretools

## 2.2 自动调参参考
1. NNI
2. TPOT

## 2.3 数据的保存与衔接  
**每个步骤，都单独的接口调用的话，数据如何衔接得上？**  
**因为不可能一个接口直接搞定整个pipeline,总还得用户参与一些中间过程。**
1. 每次都落磁盘，带上步骤编号，落到项目，目录下得tmp,每天清理。效率低下，但是可以回滚
2. 文件共享，多进程文件共享，类似RPC
https://www.cnblogs.com/xiaxuexiaoab/p/8558519.html
3. load数据并展示后，用户将所有参数设置完，然后执行训练生成报告

## 2.4 技术/包参考  
需要阅读源码并改造
1. [h2o-3](https://github.com/h2oai/h2o-3/)  （庞大，java,scala,分布式）
2. 不错，4.4k [hyperopt](https://github.com/hyperopt/hyperopt)  
3. [hyperopt-sklearn](https://github.com/hyperopt/hyperopt-sklearn)  （重复 hyperopt）
4. ++不错，5.5k，+NAS，并行，微软加持，k8s[nni](https://github.com/Microsoft/nni)  
5. [scikit-optimize](https://github.com/scikit-optimize/scikit-optimize) （有点小，star 1.7K） 
6. ++不错，6.8k，代码可读性好,并行，遗传算法 [tpot](https://github.com/EpistasisLab/tpot)  
7. [tune](https://github.com/ray-project/ray/tree/master/python/ray/tune) （有些庞大，主要是针对深度学习） 
8. [MLBox](https://github.com/AxeldeRomblay/MLBox)（有点小，star 1K）
9. ++不错，4.7k，特征工程做得多 [Featuretools](https://github.com/FeatureLabs/featuretools) 
10. [automl-gs](https://github.com/minimaxir/automl-gs) （参考设计而已）
11. [auto_ml](https://github.com/ClimbsRocks/auto_ml) （参考设计而已）
12. [auto-sklearn](https://github.com/automl/auto-sklearn)

# 参考  
1. [GitHub：AutoML论文合集](https://github.com/hibayesian/awesome-automl-papers)
2. [GitHub：搜索AutoML主题](https://github.com/topics/automl)  
3. 公众号 【AutoML前沿】  
4. 平台：  
- [h2o](https://www.h2o.ai/)
- 
