---
title: Ubuntu 18.04 LTS安装CNDeepdive
date: 2018-03-04
comments: true
categies:
  - KnowledgeComputing
tags:
  - deepdive
  - datamining
---

Deepdive是斯坦福前几年开发的知识特征提取引擎，不过项目目前已经进入维护状态。最近由于研究项目需要，准备基于CNDeepdive对中文进行知识抽取。

虽然官方最新支持到Ubuntu 16.04，而自己的系统是18.04，加之不愿折腾新系统，一个周末都在趟坑，不过尚好走通了，记录下来以飨来者。

<!-- more -->

首先，CNDeepdive可以从[OpenKG.cn](http://www.openkg.cn/tool/cn-deepdive)或[百度云盘](https://pan.baidu.com/s/1slLpYVz)下载。由于自动化安装基于deepdive发布版，在18.04上主要遇到Python依赖无法满足（读者可以自行尝试），自动化安装失败！

转而从官方源码进行编译安装（也属无奈之举），参考[Github项目](https://github.com/HazyResearch/deepdive)以及[开发者手册](https://github.com/HazyResearch/deepdive/blob/master/doc/developer.md#readme)。

**安装依赖**

```bash
git clone --recurse-submodules https://github.com/HazyResearch/deepdive.git
```
由于环境兼容性问题，需要做一些修改：

手动修改[install.Ubuntu.sh](https://github.com/HazyResearch/deepdive/blob/master/util/install/install.Ubuntu.sh)的Python依赖，去掉由于版本关系不支持的`python-software-properties`（删除所有出现）。

由于编译Deepdive时一些组件需要依赖g++-4.8，这里利用update-alternative进行g++版本管理：
```bash
sudo apt install g++-4.8
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 20  # 系统默认版本
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 20
sudo update-alternatives --config g++  # 选择g++-4.8对应数字，临时切换到该版本
```

安装运行时依赖

```bash
export NO_DOCKER_BUILD=true
export NO_MINDBENDER=true  #后面说明原因
make depends
```

**编译安装Deepdive**

```bash
make install  # to ~/local by default
```

**安装Mindbender**

Mindbender是基于deepdive的一系列知识库建立工具集。

由于在当前系统环境，顺利安装后报JS语法错误，为了节省时间，该组件直接采用[官方文档](https://github.com/HazyResearch/mindbender)独立安装。

至此，英文版的Deepdive安装完成！

**安装CNDeepdive**

完成了CNDeepdive要求的第一步，此时进入CNDeepdive目录，运行nlp_setup.sh，配置本地中文stanford环境。

至此，CNDeepdive安装完成！

后续，参考[CNDeepdive文档](http://openkg1.oss-cn-beijing.aliyuncs.com/478e0087-8dd6-417c-9a49-4ce12f5ec22c/tutorial.pdf)进行中文实例测试，不赘言。

**恢复系统环境**

```bash
sudo update-alternatives --config g++  # 选择g++-7对应数字，恢复系统默认版本
```
