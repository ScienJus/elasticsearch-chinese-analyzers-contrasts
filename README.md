# elasticsearch-chinese-analyzers-contrasts

Elasticsearch中文分词插件分词效果对比（Ik、Ansj、Mmseg和Jieba）

==================

~~[在线测试地址][1]，还没来得及写个样式~~

由于Elasticsearch太吃内存了，开着什么都不干都要将近300mb，备胎服务器带不动就给关了。

后来仔细想了下，就这么三种其实也没什么可对比的……给出我认为的评价吧：

- Ik：由 [@medcl][2] 大神维护，迭代速度肯定是没得说的，始终能追上Elasticsearch的最新版本。有两种分词模式，支持热词库，用户最多。
- Mmseg：同样由大神维护，但是分词效果在我使用中觉得相当不好，而且三种分词模式的效果完全相同。
- Ansj：由作者维护，可能会落后一些小版本，但是也已经支持2.x版本了。分词效果也相当不错，有两种分词模式，支持基于Redis配置歧义词。

个人推荐顺序 Ik > Ansj > Mmseg

==================

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
[2]: https://github.com/medcl
