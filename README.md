# ChineseNER
本项目使用的是python2.7

对命名实体识别不了解的可以先看一下<a href="https://blog.csdn.net/buppt/article/details/81180361">这篇文章</a>。

这是最简单的一个命名实体识别BiLSTM+CRF模型。

data文件夹中有三个开源数据集可供使用，玻森数据 (https://bosonnlp.com) 、1998年人民日报标注数据、MSRA微软亚洲研究院开源数据。其中boson数据集有6种实体类型，人民日报语料和MSRA一般只提取人名、地名、组织名三种实体类型。

先运行数据中的py文件处理数据，供模型使用。
然后运行pytorch或tensorflow中的train.py。
模型会保存到相应的model文件夹中，可以在训练好的模型的基础上继续训练。
## pytorch版
直接用的<a href="https://pytorch.org/tutorials/beginner/nlp/advanced_tutorial.html">pytorch tutorial</a>里的Bilstm+crf模型.

运行train.py训练即可。由于使用的是cpu，而且也没有使用batch，所以训练速度超级慢。想简单跑一下代码的话，建议只使用部分数据跑一下。pytorch暂时不再更新。

## tensorflow版
运行train.py训练即可，使用的是tensorflow封装好的crf，使用了batch，训练速度比较快。


不定期增加其他修改。。


参数并没有调的太仔细，boson数据集的f值在70%~75%左右，人民日报和MSRA数据集的f值在90%左右。（毕竟boson有6种实体类型，另外两个只有3种。）





## 更新日志
2018-9-15 增加tensorflow版本。

2018-9-17 增加1998年人民日报数据集和MSRA微软亚洲研究院数据集。

2018-9-19 简单修改了代码风格，将model提取出来，方便以后拓展。
