# elasticsearch-chinese-analyzers-contrasts

Elasticsearch中文分词插件分词效果对比（Ik、Ansj、Mmseg和Jieba）

[在线测试地址][1]，还没来得及写个样式

可以在安装分词插件之前，先在这个网站上对比一下每个分词插件的效果，选择最合适的插件和模式，节约了自己安装和调试的时间。

目前的Elasticsearch版本是1.7.1，已支持以下分词插件：

- Ik
- Ansj
- Mmseg

共有以下几种模式进行对比：

- ik_max_word
- ik_smart
- ansj_query
- ansj_index
- mmseg_complex
- mmseg_maxword
- mmseg_simple

注：发现mmseg的几种模式分词结果几乎一样，不知道是我配置的有问题还是本来就这样。

暂时无法对比Jieba分词，原因是对应的Elasticsearch分词插件已经半年没有更新了，我Clone源码打包会报错。并且Jieba目前还没有支持Elasticsearch 2.X版本的更新，所以无法进行对比（一开始就是为了将Jieba加入对比才使用的1.7.1版本，另外三个插件都已经支持2.X版本了）。


[1]: http://es.scienjus.com/
