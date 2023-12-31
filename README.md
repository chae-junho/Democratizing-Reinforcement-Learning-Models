# Democratizing Reinforcement Learning Models
## （神经网络+决策树+支持向量机+随机森林+朴素贝叶斯+强化学习）的综合模型
**思想：秉承智者共治的理念，我们致力于降低训练成本，使得即使没有强大的GPU设备的组织或个人也能够使用AI技术。为此，我们训练了5个人工智能分类模型，并通过与环境（即人类）互动，使每个模型获得相应的话语权重。最初，我们给予训练时间最长的神经网络模型最高的权重，即0.6，而其他模型则为0.1。最后，我们采用强化学习的方法对每个模型的话语权重进行优化。**
***
1. 首先，我要感谢word2vec的中文预训练模型([wiki_word2vec_50.bin](word2vec_data%2Fwiki_word2vec_50.bin))，它为我们的工作提供了重要的基础。

2. 其次，我们构建了五种模型，包括朴素贝叶斯、决策树、随机森林、支持向量机以及基于BiLSTM-attention的神经网络模型。其中，基于BiLSTM-attention的神经网络模型是一种将双向长短期记忆网络（Bidirectional LSTM）和注意力机制（Attention）结合在一起的模型。

3. 最后，我们采用了Q-learning算法进行强化学习，通过与用户的交互不断调整权重，以提高评论分类模型的性能和准确性。在每次预测后，根据用户的反馈更新权重，并使用学习率和折扣因子来平衡奖励的重要性。通过利用多个模型和动态权重调整的方式，我们实现了更准确的评论分类。
***
## 项目文件介绍：
### 1. 关于神经网络（nn）：
1. [nn_Config.py](nn%2Fnn_Config.py)：有神经网络相关的配置信息。

2. [nn_DataProcess.py](nn%2Fnn_DataProcess.py)：运行此文件可以获得此项目会用到的.txt文件。

3. [nn_main.ipynb](nn%2Fnn_main.ipynb)：可以得到模型。

### 2. 关于朴素贝叶斯（Bayes）：
1. [Bayes_Config.py](Bayes%2FBayes_Config.py)   :配置信息
2. [Bayes_DataProcess.py](Bayes%2FBayes_DataProcess.py)：数据预处理
3. [Bayes_main.ipynb](Bayes%2FBayes_main.ipynb)：训练模型
4. [test_bayes.ipynb](Bayes%2Ftest_bayes.ipynb)：测试模型

### 3. 关于随机森林（RandomForest）：
1. [RandomForest_Config.py](RandomForest%2FRandomForest_Config.py)：配置信息
2. [RandomForest_DataProcess.py](RandomForest%2FRandomForest_DataProcess.py)：数据预处理
3. [RandomForest_main.ipynb](RandomForest%2FRandomForest_main.ipynb)：训练模型
4. [test_randomForest.ipynb](RandomForest%2Ftest_randomForest.ipynb)：测试模型

### 4. 关于支持向量机（SVM）：
1. [SVM_Config.py](SVM%2FSVM_Config.py)：配置信息
2. [SVM_DataProcess.py](SVM%2FSVM_DataProcess.py)：数据预处理
3. [SVM_main.ipynb](SVM%2FSVM_main.ipynb)：训练模型
4. [test_svm.ipynb](SVM%2Ftest_svm.ipynb)：测试模型

### 5. 关于决策树（DecisionTree）：
1. [DecisionTree_Config.py](DecisionTree%2FDecisionTree_Config.py)：配置信息
2. [DecisioTree_DataProcess.py](DecisionTree%2FDecisioTree_DataProcess.py)：数据预处理
3. [DecisionTree_main.ipynb](DecisionTree%2FDecisionTree_main.ipynb)：训练模型
4. [test_decisionTree.ipynb](DecisionTree%2Ftest_decisionTree.ipynb)：测试模型

### 6. [ml_predict.py](ml_predict.py)：
**朴素贝叶斯，随机森林，支持向量机，决策树的预测逻辑。**

### 7. [nn_predict.py](nn%2Fnn_predict.py)
**神经网络的预测逻辑。**

### 8. 关于强化学习
1. [policy_Q.py](nn%2Fpolicy_Q.py)：使用强化学习的思想，通过跟人类交互，优化每个模型的话语权权重。
***
*ps：本项目参考了搜索引擎，网友们分享的代码。感谢这个万物开源的时代和精神！*



