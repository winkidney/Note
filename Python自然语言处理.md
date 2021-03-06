#第一章
##一些工具的使用
+ python列表解析
+ fdist1 = nltk.book.FreqDist(text1）
+ FreqDist.plot(50,cumulative=True)查看频率前50的词的累计（cumulative）图
+ fdist1.hapaxes()查看只出现一次的词
+ text*.collocations()统计出现的搭配词（不经常出现且无法被其他词替换的词语搭配，比如red wine，换成blue wine就会很奇怪。）

##一些概念
+ 词义消歧：使用上下文消除歧义
+ 指代消解：使用上下文理解代词所代指的对象
+ 自动生成语言：
    + 自动问答
    + 机器翻译
        + 文本对齐：使用两种语言的相似文本预料库，对其中达到同义部分进行对齐，使用词典等工具建立新的翻译模型。
    + 人机对话系统
        <code>
        语音分析->形态和次法分析->解析->上下文推理->
                                                    应用推理和执行
        语音合成<-形态实现    <-句法实现<-话语规划<-
        |发音模型|形态规划  |词汇和语法| 话语背景   |   领域知识   |
        |语位学  |形态学    |句法      | 语义       |    推理      |
        </code>

##NLTK 工具函数和工具类
+ 英文分词：nltk.word_tokenize(src_text)
+ 文本对象:nltk.Text(tokens) - tokens必须是一个词汇列表
+ 获取NLTK自带资源：path = ntlk.data.find('relative_path_of_source_file')
