
# 多语言预训练JoveBM模型

*****************************************************************************************************
*我们的目标不是追求更大的模型规模，而是轻量级但更强大，同时对部署和工业落地更友好的模型。

*本系列模型采用目前主流的Roberta架构，多语言版采用XLM-Roberta

*从语料上，中文单语版从超1T的中文语料中筛选出100G+的高质量文本参与训练，多语言版在CC100基础上，新增13个语种非平行语料，并加入数十G的平行语料
         
中文预训练RoBERTa模型-下载
模型在两台A6000服务器(8*48G*2)训练50天而成
-------------------------------------------------
Roberta-zh-large： <a href="https://pan.baidu.com/s/155fo1jH-bACcdM27rACinQ">百度网盘</a>下载 TensorFlow版本，Bert直接加载

Roberta-zh-large： <a href="https://pan.baidu.com/s/1lVxTuBvorClo-7uoCAO7kQ">百度网盘</a>下载 pytorch版本，Bert直接加载

Roberta-zh-large： <a href="https://pan.baidu.com/s/1zaMV5lNF2Ar3l8L4bZcsLQ">百度网盘</a>下载 Uer-Py版本，腾讯开源工具(Uer_Py)直接加载


发布计划 Release Plan：
-------------------------------------------------
1、24层RoBERTa模型(roberta_l24_zh)，使用100GG文件训练（纯数据版本）， 10月28日

2、24层RoBERTa模型(roberta_l24_zh)，使用100GG文件训练（知识+数据）， 11月30日

3、24层RoBERTa模型多语言版本(roberta_l24_multi)，使用100GG文件训练（知识+数据）， 11月30日

4、未完待续……

效果测试与对比 Performance 
-------------------------------------------------
### CLUE-NER

| 模型 | 线上F1 |
| :------- | :---------: |
| BI-LSTM | 70 |
| Bert | 78.82 | 
| RoBERTa-wwm-large-ext | 80.42 | 
| *Gtcom-zh-Large** | **80.44** |


###  CLUE-NER分类(Acc)

| 模型 | All-Acc | TNEWS1.1 | IFLYTEK | AFQMC | CMNLI | WSC1.1 | CSL |
| :------- | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: | :---------: |
| BI-LSTM | 61.2 | 49.53 | 53.27 | 69 | 58.5 | 61.1 | 75.8 |
| Bert | 68.77 | 56.58 | 60.29 | 73.7 | 79.69 | 62 | 70.36 |
| RoBERTa-wwm-large-ext | 70.1 | 56.94 | 60.31 | 74.04 | 80.51 | 67.8 | 81 |
| *Gtcom-zh-Large** |  **75.05** | 59.41 | 62.5 | 76.39 | 82.64 | 84.54 | 84.9 |

联系方式（邮箱）
-------------------------------------------------
XXXXXXXXXXXXXXXXX
