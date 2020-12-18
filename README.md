# TX-WORD2VEC

腾讯开源的word2vec模型。

原版15个G，一般爱好者很难玩出来。

所以做了一些小的。方便大家使用。


5000-small.txt 这个有5000词，可以下下来玩玩

45000-small.txt 这个有4.5w的词，已经能解决很多问题了

70000-small.txt 7w词  133MB
https://pan.baidu.com/s/1DprHD8HwEqkWRBG0ss2y1A

100000-small.txt 10w词 190MB
https://pan.baidu.com/s/1KqPOwfrw3KoLJqTsCUdriA

500000-small.txt 50w词 953MB
https://pan.baidu.com/s/1SGwxpGW8HjYw8HdKQUB8Gw

1000000-small.txt 100w词 1.9GB
https://pan.baidu.com/s/1ObstPl7R8o1L98Ag9owGiw

2000000-small.txt 200w词 3.8GB
https://pan.baidu.com/s/1hmCiMandgyedjmP520_Aog

再大就自己去下载吧

https://ai.tencent.com/ailab/nlp/en/embedding.html



## 如何使用

### 读取模型

```python
from gensim.models import KeyedVectors

model = KeyedVectors.load_word2vec_format("50-small.txt")
```
### 把玩模型

```python
model.most_similar(positive=['女', '国王'], negative=['男'], topn=1)

model.doesnt_match("上海 成都 广州 北京".split(" "))

model.similarity('女人', '男人')

model.most_similar('特朗普',topn=10)

```

### 深度模式示例

使用LSTM模型，根据豆瓣评论，预测打分。

首先下载豆瓣的数据

豆瓣评论数据149M
https://pan.baidu.com/s/1WbqoCKsmrnpf6n5ZTV-fKA

然后下载库对应的分词包。
https://pan.baidu.com/s/19busyY1yysbOgdYWxIaIQA

加载70000字典前
![Image text](https://github.com/cliuxinxin/TX-WORD2VEC-SMALL/blob/master/pics/WX20181025-142826%402x.png)

加载70000字典后
![Image text](https://github.com/cliuxinxin/TX-WORD2VEC-SMALL/blob/master/pics/WX20181025-142850%402x.png)


代码文件见
Use Tencent Word Embeddings with douban datasets.ipynb

抛转引玉，如果有哪位朋友有功夫更新其他的模型或者数据库，还可以request pull

有问题也可以开issue


