# 2023BJTU机器学习大作业
本次大作业需要解决的问题是小样本分类问题，即每个类别给定少量的训练图像，在推理时预测出每张测试图像的类别

## Kaggle邀请链接
请同学们点击下方链接进入比赛

https://www.kaggle.com/t/e29c5e16f7f944e7be29fbc6a5be4d69

## 题目说明
### 数据
```
data/
|–– train/              # 训练集：960张图片
|–– test/               # 测试集：6170张图片
|–– class_to_id.json    # 类别到序号的映射
|–– train.tsv           # 训练集图像数字标签
```
除给定的960张训练图片外， 不允许额外搜集外部数据来训练模型

### 评估
需要提交的文件：impreds.csv，包含测试集6170张图像的预测标签，行数和测试集图像id对应
```
14 # 测试集第1张图像的预测标签
4  # 测试集第2张图像的预测标签
10
3
2
...
```

评估指标: 测试集准确率
$$
Accuracy =  \frac{测试集中正确分类的数量}{测试集总数量}
$$

### 预训练模型要求

只能使用imagenet预训练版本的Restnet50模型， 或者OpenAI提供的CLIP-RN50模型权重， 不允许使用其他的预训练模型

### 复现要求
比赛结束后， 所有队伍需要提交可复现的项目文件夹


## Baseline
### 环境安装
安装pytorch环境
```
pip install -r requirements.txt
```
安装CLIP
```
pip install git+https://github.com/openai/CLIP.git
```
### 运行Baseline
见 Baseline.ipynb
