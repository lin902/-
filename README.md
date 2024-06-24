# 动手学大模型应用开发
可运行代码在jupyter文件夹中，详细笔记[csdn专栏](https://blog.csdn.net/weixin_49206002/category_12706043.html)
1. **大模型简介**，何为大模型、大模型特点是什么、LangChain 是什么，如何开发一个 LLM 应用，针对小白开发者的简单介绍；
2. **如何调用大模型 API**，本节介绍了国内外知名大模型产品 API 的多种调用方式，包括调用原生 API、封装为 LangChain LLM、封装为 Fastapi 等调用方式，同时将包括百度文心、讯飞星火、智谱AI等多种大模型 API 进行了统一形式封装；
3. **知识库搭建**，不同类型知识库文档的加载、处理，向量数据库的搭建；
4. **构建 RAG 应用**，包括将 LLM 接入到 LangChain 构建检索问答链，使用 Streamlit 进行应用部署
5. **验证迭代**，大模型开发如何实现验证迭代，一般的评估方法有什么；

本项目主要包括三部分内容：

1. **LLM 开发入门**。V1 版本的简化版，旨在帮助初学者最快、最便捷地入门 LLM 开发，理解 LLM 开发的一般流程，可以搭建出一个简单的 Demo。
2. **LLM 开发技巧**。LLM 开发更进阶的技巧，包括但不限于：Prompt Engineering、多类型源数据的处理、优化检索、召回精排、Agent 框架等（待更新）
3. **LLM 应用实例**。引入一些成功的开源案例，从本课程的角度出发，解析这些应用范例的 Idea、核心思路、实现框架，帮助初学者明白其可以通过 LLM 开发什么样的应用。（待更新）

# 通用环境配置
```python
conda create -n llm-universe python=3.10 #创建虚拟环境
conda activate llm-universe #激活
#进入到想要复制的个人目录 cd /hpc2hdd/home/gbian883
git clone git@github.com:datawhalechina/llm-universe.git #克隆
cd llm-universe #进入目录
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple #安装包
# conda info --envs 查看当前虚拟环境的路径

```
nltk库下载
```python
# cd /root 变成cd /hpc2hdd/home/gbian883
git clone https://gitee.com/yzy0612/nltk_data.git  --branch gh-pages
cd nltk_data
mv packages/*  ./  #将packages文件夹中的所有文件和子文件夹移动到当前目录（.表示当前目录）
cd tokenizers
unzip punkt.zip
cd ../taggers  #返回到上一级目录，再进入taggers子目录
unzip averaged_perceptron_tagger.zip

```

