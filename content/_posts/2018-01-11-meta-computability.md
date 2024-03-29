---
layout: post
title: "元数据的可计算化反 II"
subtitle: "The Computability of Metadata (Part 2)"
date: 2018-01-11
author: "Jamin Chen"
header-img: "img/post-bg-universe.jpg"
tags: ["Metadata", "Computability"]
---

题解：这个《元数据》系列本计划介绍一种有关数据的科技讯息，上篇完成后有读者反馈并非人人都懂技术，首当其冲便是这个看不懂的反人类题目。正巧元旦节期出游了趟鲁迅先生故居，从繁糜商业气息中依稀有些关于那个过往时代的见闻。细思之下，我所目标分享的，其实不是数据也不是科技本身，而是这个和数据科技息息相关的时代。而这些狄更斯多年前已经总结完了，无妨对于当下这个时代，填些骨肉，说道说道我眼中这个“失控”的数据时代。

在上一篇中我们提到了人类百万年进化出的一项功能“记忆惰性”：对纷繁复杂的外界信息经过深加工，以类似偷懒的方式，形成记忆知识并储存在大脑神经元中。因此随着年龄的增长，记忆神经元退化，甚至部分脑细胞老化导致相关知识也随之消失，也就是医学上的“阿尔兹海默症”。

人类在进化过程中，不断寻找新的工具弥补自身的短板。从蒸汽革命到电气革命到计算机革命，从体力解放到脑力解放，一次次的技术更新在不断刷新人类的工具包，也不断刷新着追求更大的解放的野心。

在最近一次的计算机革命中（开始于20世纪五六十年代），人们努力寻找各种工具克服自身的“记忆惰性”：不想耗费能量处理复杂的计算，电子计算机由此诞生（电影《模仿游戏》）；服务器代替了图书馆，互联网网页的扩张速度远远超过了书本的页数增长；社交网络帮你记录了所有的朋友关系和动态，大脑所需的记忆便是一个网址以及账号；机器学习算法和AI智能技术的最新进展，让人们再次萌生冲动毅然准备放弃这个上帝亲自创造的智慧灵魂。

正是由于人类的“记忆惰性”这一生物制约，促进了20世纪中后期以来在计算机技术上的不断推陈出新，不断追求极致。这是最好的时代。

诚然，一边是进化了百万年以上的躯体，一边是从诞生到繁荣不过六七十年的技术，二者所包含的信息匹敌远远不在一个量级。我们还有很长的路要走。人们诸多的憧憬和YY。这也是最坏的时代，一个有些失控的时代。

失控不仅在主观，也在客观。计算信息技术在初期表现出很强的经济效应，这种繁荣挤压了以往的经济领域，更多的资源将目光投向“新欢”，而冷落了“旧爱”。

这一繁荣正面上得益于两个信息不对称：一个早期高科技的局部繁荣与全球落后之间的不对称，这个不对称造就了少数几个早期信息强国；另一个是高科技扩散在时间上的不对称，这个不对称造就了一些较早接触到这一先机的富裕群体（体现在个人层面便是互联网业鼓吹的一夜暴富）。

在整个发展尺度上看的时候，我们依然处在计算机革命的余波之中，只是波的能量在不断降低，变得有些“波澜不惊”。因为随着信息的传播时间越长、范围越广，上述两个不对称性消失得越快。结合当下，“互联网+”的声嘶力竭的呐喊，仅仅是这一波澜上的一次小小的回音，毕竟，这只是一次努力寻找当前世界中信息不对称的缝隙，而不是发现一个处女的旷地或峡谷。

而之前高不对称的信息时代积累的经济红利，就像一头被困的发情公牛，也对这个所谓的“余波”阶段做了最好的注脚。在商业发展初期，尤其是农业为支撑经济的时代，商业的短期繁荣往往预示着农业的衰弱（吴晓波《浩荡两千年》）。类似地，在出现新的信息不对称机遇之前，以往的资本积累开始玩“金钱游戏”，涌入各种投机市场，此时人的欲望在金钱游戏中被利用（想想现在的金融和投资市场）。这种投机短期来讲对于实体经济有些甜头，但是长期来讲可是会伤筋动骨的。

失控也蕴含着机遇。在计算机革命初期较大的信息化行动之后，人类不仅积累的财富，同时造就了一台覆盖全球的数字机器。这一机器以互联网为载体，连接着数以百亿记的各类数字化信息化设备，7x24小时马力全开地产生着源源不断比特数据。

这一机器在不断自我完善，在便捷我们人类生活的同时，也在不断挑战我们人类自身。好吧，不要嫌我烦，这里又要提我们自身的生物约束，“记忆惰性”。

我们本以为这台机器会帮我们很好的保留信息，可惜的是，一个网页的平均寿命数量级在1000天左右（10.1109/JCDL.2014.6970226）。“记忆惰性”本能地促使人们开始认真思考，如何更好地将我们所在时代的信息有效的留存下来？换句话说，如何从这些海量的数据中萃取出有价值的信息，并借助机器或人类本身，将其存储为知识。

这一内在的冲动，也正是我眼中的这些年技术发展的内在驱动。这种冲动如此强烈，甚至有些焦虑的迹象，以至于可以在短期内，被一个“人狗大战”（记得阿法狗AlphaGo？）的报道搞得热血沸腾，媒体也拿出了可以媲美当年人类登月前后的脑洞和激情。《星球大战》和《星际迷航》系列便诞生在那个时候，很多国内外创业者都表示喜欢这两部作品，或许因为大家都处在相似的年代吧！

这一内在的冲动也并非纯粹的热血。21世纪初几乎火遍全球的“大数据”（也许除了南北极和少有的几个原始部落），便是人们拿出的针对这一焦虑的初期方案。这个方案所起到的实际效果，在笔者看来，布道的成效远大于实际效益本身。

从布道的角度，人们开始认真思考计算机革命的初期不对称性即将消失的时候，如何面对数字机器7x24小时的生产力和人类自身“记忆惰性”之间的矛盾。这一矛盾实际上在积累新的不对称性，新的不对称性同时需要新的能力去解决（当然不仅仅是科技，包括经济、政治、甚至人类认知本身的提升）。这种新的不对称性我们在会详述。

集体的共识往往是在集体的焦虑中达成的。

这几年的云计算、大数据、人工智能技术热，无非在帮助人们从计算、数据、算法维度探索一条走出当前焦虑的道路。这些技术本身并不是我想讨论的重点，否则容易为一木而舍一林（虽然平时80%的时间都在做这些事情）。

这条道路本身建立在新的不对称性之上。不过在笔者看来，这些在新的不对称性积累的初期阶段，新的科技都是相辅相成的，在未来的某个时间、空间点上，大家将会汇聚一起（当然发展过程中也在不断融合），产生更多的突破和能量，从另一个层次上破解新的不对称性难题。

因此可以说，我们处在一个失控、但又可能是最好的时代。这时候请我们再默念下略有修改的狄更斯先生的箴言，会有更多感触：

这是一个最坏的时代，这是一个最好的时代；
这是一个愚蠢的年代，这是一个智慧的年代


下篇摘要：

在数字化世界里，信息被“拍平”，转换成文字图像，以“超高清”方式记录在网络媒介上。这种“超高清”方式喻指，一个故事的梗概和细节同时被记录，且表示为无差别的表达形式（如文字或像素）。例如，一篇数字化了的文章记录的故事，梗概部分不会随着时间流逝而凸显，细节的部分也不会随着时间流逝而消失。如何借助于人类的“记忆惰性”，实现从数据-->信息-->知识的蜕变的同时，降低人类个体获取信息的成本。这一趋势开始于21世纪初，新技术的蓬勃带来了“信息孤岛”效应，以及数据壁垒，进而造成新的信息不对称....
