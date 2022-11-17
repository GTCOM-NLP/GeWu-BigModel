
# 格物-多语言预训练模型-轻量版

## 模型简介
* 我们的目标不是追求更大的模型规模，而是轻量级但更强大，同时对部署和工业落地更友好的模型。

* 本系列模型采用目前主流的Roberta架构，多语言版采用XLM-Roberta

* 中文单语版从超1T的中文语料中筛选出100G+的高质量文本参与训练，语料来自百科、论坛、新闻、科技论文等，并采用高效分类方法，覆盖军事、政治、经济、科技等14个领域，充分增强数据的丰富度，同时增强模型的通用性

* 多语言版在CC100基础上，新增13个语种非平行语料，并加入数十G的平行语料，实现113个语种的大规模预训练

* 中文单语版加入知识增强，包括词性、嵌入实体MASK，以及知识链接对照式增强；

* 多语言预训练在原有XLM-Roberta基础上增加双语对齐策略，增强多语言之间的语义表示
         
## 模型下载
### 1. 格物-中文纯数据预训练模型-轻量版（GeWu-Lite-pd）
**该模型率先开源共享使用，该模型在两台A6000服务器(8x48Gx2)训练50天而成，下载地址如下：**

* GeWu-Lite-pd： <a href="https://pan.baidu.com/s/19k-5aLOe4pW_1qu8yAcBwA">百度网盘(验证码zyyt)</a>下载 TensorFlow版本，Bert直接加载

* GeWu-Lite-pd： <a href="https://pan.baidu.com/s/1CvWxKCwV3ltIsUWx6R9xlQ">百度网盘(验证码zyyt)</a>下载 pytorch版本，Bert直接加载

* GeWu-Lite-pd： <a href="https://pan.baidu.com/s/1ZEtWBpbPBBXZcgSZqT67_w">百度网盘(验证码zyyt)</a>下载 Uer-Py版本，腾讯开源工具(Uer_Py)直接加载

### 2. 格物-中文知识增强预训练模型-轻量版（GeWu-Lite-kg）

敬请期待。。。

### 3. 格物-多语言预训练模型-轻量版（GeWu-Lite-ml）

敬请期待。。。

## 发布计划 Release Plan：
1、格物-中文纯数据预训练模型-轻量版（GeWu-Lite-pd）模型，纯数据版本，无知识增强版， 10月31日

2、格物-中文知识增强预训练模型-轻量版（GeWu-Lite-kg），知识增强版， 11月30日

3、格物-多语言预训练模型-轻量版（GeWu-Lite-ml），涵盖113个语种的多语言版，待定

4、个性化跨语言文本生成大模型，待定

5、大模型持续推进中，敬请期待。。。

效果测试与对比 Performance 
-------------------------------------------------

###  CLUE分类(Acc)

| 模型 | All-Acc | TNEWS1.1 | IFLYTEK | AFQMC | CMNLI | WSC1.1 | CSL |
| :------- | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: |
| BI-LSTM | 61.2 | 49.53 | 53.27 | 69 | 58.5 | 61.1 | 75.8 |
| Bert-base | 68.77 | 56.58 | 60.29 | 73.7 | 79.69 | 62 | 80.36 |
| Bert-wwm-ext | 68.75 | 56.84 | 59.43 | 74.07 | 80.42 | 61.1 | 80.63 |
| ERNIE-base | 68.55 | 58.33 | 58.96 | 73.83 | 80.29 | 60.8 | 79.1 |
| RoBERTa-large | 71.70 | 57.86 | 62.55 | 74.02 | 81.7 | 72.7 | 81.36 |
| XLNet-mid | 68.58 | 56.24 | 57.85 | 70.5 | 81.25 | 64.4 | 81.26 |
| ALBERT-XXlarge | 71.04 | 59.46 | 62.89 | 75.6 | 83.14 | 61.54 | 83.63 |
| ALBERT-Xlarge | 68.92 | 57.36 | 59.5 | 69.96 | 81.13 | 64.34 | 81.2 |
| ALBERT-large | 67.91 | 55.16 | 57 | 74 | 78.77 | 62.24 | 80.3 |
| ALBERT-base | 67.44 | 55.06 | 56.58 | 72.55 | 77.58 | 64.34 | 78.5 |
| ALBERT-tiny | 62.61 | 53.35 | 48.71 | 69.92 | 70.61 | 58.5 | 74.56 |
| RoBERTa-wwm-ext | 70.1 | 56.94 | 60.31 | 74.04 | 80.51 | 67.8 | 81 |
| RoBERTa-wwm-large | 72.83 | 58.61 | 62.98 | 76.55 | 82.12 | 74.6 | 82.13 |
| Mengzi-BERT-base | 74.71 | 57.97 | 60.68 | 74.58 | 82.12 | 87.5 | 85.4 |
| ***GeWu-Lite-pd**** |  **75.05** | 59.41 | 62.5 | 76.39 | 82.64 | 84.54 | 84.9 |

注：其他模型评测结果数据直接来自于：

https://github.com/CLUEbenchmark/CLUE

https://huggingface.co/Langboat/mengzi-bert-base

### CLUE-NER

| 模型 | 线上F1 |
| :------- | :---------: |
| BI-LSTM | 70 |
| Bert-base | 78.82 | 
| RoBERTa-wwm-large-ext | 80.42 | 
| ***GeWu-Lite-pd**** | **80.44** |

## 问题反馈：
目前团队仍在不断研发和优化中，不足的地方希望批评指正

如有问题，请在GitHub Issue中留言。
