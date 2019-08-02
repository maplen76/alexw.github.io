---
layout: post
tags: ConfusionMatrix
date: 2018-12-20 18:06
title:  "Confusion Matrix"
---

|  | T | F |
|---|---|---|
| Positive | TP | FP |
| Negative | FN | TN |
TP: 预测结果是Postive这个命题本身是TRUE
TF: 预测结果是Negative这个命题本身是TRUE
FP: 预测结果是Postive这个命题本身是FALSE
FN: 预测结果是Negative这个命题本身是FALSE

Recall = TP/(TP+FN) ,所有原本是postive的样本中被正确预测到的占比  
- 之所以叫Recal就是对原本情况的追溯

Precision = TP/(TP+FP),  所有被预测为Positive的样本中**被正确预测**的占比  
- 预测结果被分为两部分，正确预测和错误预测

Accuracy = (TP+TN)/Total, 所有样本被正确预测的占比  
 
为什么用RoC来衡量分类器（classifer）的好坏？  
- 期望 **最大化** True Positive 的比例，同时 **最小化** False positive 的比例 
- 极端情况是TPR=1， FPR=0
