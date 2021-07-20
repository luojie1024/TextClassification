

# 文本分类
> TextCNN，TextRNN基于pytorch

## [免费教学视频](https://www.imooc.com/learn/1311)

## 介绍
模型介绍、数据流动过程：
数据以字为单位输入模型，预训练词向量使用 

搜狗新闻 Word+Character 300d
+ [搜狗词向量 GitHub下载](https://github.com/Embedding/Chinese-Word-Vectors)
+ [搜狗词向量 百度云下载](https://pan.baidu.com/s/14k-9jsspp43ZhMxqPmsWMQ)  

## 环境
python 3.7  
pytorch 1.1  
tqdm  
sklearn  
tensorboardX

## 中文数据集
[清华数据集，THUCNews](http://thuctc.thunlp.org/) ，抽取了20万条新闻标题，已上传至github，文本长度在20到30之间。一共10个类别，每类2万条。

类别：财经、房产、股票、教育、科技、社会、时政、体育、游戏、娱乐。

数据集划分：

数据集|数据量
--|--
训练集|18万
验证集|1万
测试集|1万


### 更换自己的数据集
 - 如果用字，按照我数据集的格式来格式化你的数据。  
 - 如果用词，提前分好词，词之间用空格隔开，`python run.py --model TextCNN --word True`  
 - 使用预训练词向量：utils.py的main函数可以提取词表对应的预训练词向量。  


## 效果

模型|acc|备注
--|--|--
TextCNN|91.22%|Kim 2014 经典的CNN文本分类
TextRNN|91.12%|BiLSTM 

## 使用说明
```
cd Chapter4/Chinese-Text-Classification/

# 训练并测试：
# TextCNN
python run.py --model TextCNN

# TextRNN
python run.py --model TextRNN

```

## 参数
模型都在`Chapter4/Chinese-Text-Classification/models`目录下，超参定义和模型定义在同一文件中。  


## 参考
[1] Convolutional Neural Networks for Sentence Classification  
[2] Recurrent Neural Network for Text Classification with Multi-Task Learning  
[3] Attention-Based Bidirectional Long Short-Term Memory Networks for Relation Classification  
[4] Recurrent Convolutional Neural Networks for Text Classification  
[5] Bag of Tricks for Efficient Text Classification  
[6] Deep Pyramid Convolutional Neural Networks for Text Categorization  
[7] Attention Is All You Need  
