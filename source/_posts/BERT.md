---
title: BERT
date: 2022-09-09 13:07:27
tags: ['bert','transformer']
categories: ['深度学习' ]
index_img: /img/BERT.jfif
banner_img: /img/default.jpg
category_bar: true
---

BERT（Bidirectional Encoder Representation from Transformers），基于transformer的双向编码表示，它是一个预训练模型，模型训练时的两个任务是预测句子中被掩盖的词以及判断输入的两个句子是不是上下句。在预训练好的BERT模型后面根据特定任务加上相应的网络，可以完成NLP的下游任务，比如文本分类、机器翻译等。

# 模型输入

在BERT中，输入的向量是由三种不同的embedding求和而成，分别是：

1. wordpiece embedding：单词本身的向量表示。WordPiece是指将单词划分成一组有限的公共子词单元，能在单词的有效性和字符的灵活性之间取得一个折中的平衡。

2. position embedding：将单词的位置信息编码成特征向量。因为我们的网络结构没有RNN 或者LSTM，因此我们无法得到序列的位置信息，所以需要构建一个position embedding。构建position embedding有两种方法：BERT是初始化一个position embedding，然后通过训练将其学出来；而Transformer是通过制定规则来构建一个position embedding

3. segment embedding：用于区分两个句子的向量表示。这个在问答等非对称句子中是用区别的。

   BERT模型的输入就是wordpiece token embedding + segment embedding + position embedding，如图所示

# 网络结构

# 模型预训练

https://blog.csdn.net/u011412768/article/details/108015783