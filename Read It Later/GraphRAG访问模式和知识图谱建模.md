---
date: "2024-12-02T19:36:21+08:00"
url: "https://zhuanlan.zhihu.com/p/9423492969"
Readed: false
status:
---
![[Read It Later/attachments/ae02f1ce05d0ac133730c63fac0f6d18_MD5.jpg]]

@TOC\[1\]

- • 什么是GraphRAG
- • 了解文本分块
- • 检索模式
- • 图谱建模

- • 相关概念
- • 图结构

[http://graphrag.com](https://link.zhihu.com/?target=http%3A//graphrag.com)\[2\]是一个开源项目，收集了围绕GraphRAG的相关资源，目前正在快速收集大家的投稿。深入阅读这些文档将帮助大家将`GraphRAG`技术应用于实际项目，同时拓宽对图数据和知识图谱的理解。

检索增强生成（RAG）是一种通过将大型语言模型（LLM）与事实数据结合的方式，以减少幻觉并扩展问答所需的信息。用户的问题会被用来从一个或多个数据源中检索相关信息，这些信息为生成答案提供了事实依据。随后，将增强后的提示和原始用户问题一起传递给 LLM，以生成最终的答案。

GraphRAG是一种基于图结构的检索机制，相比纯文本搜索（或矢量搜索），它能够提供更细粒度和更相关的上下文信息。这是因为它能够利用知识图谱中关于许多领域的丰富知识表示。

## **什么是GraphRAG**

GraphRAG是基于知识图谱的检索增强生成（RAG）技术。

## **了解文本分块**

文本文档可以是简短的（例如社交媒体帖子或评论），也可以是非常长的（例如书籍）。

由于较长的文本文档通常涉及多个不同的主题，并按照顺序排列（有时还包含引用），因此将其拆分为更小、语义连贯并专注于单一主题的部分是非常理想的。

这个将文档拆分成小块的过程被称为“分块”（Chunking）。

以下是几种常见的分块策略：

- • 拆分（Splitting）：将文档拆分成大小相等的部分（按字符或词元数量），可选择性地加入重叠（典型的大小为250-500个词元，重叠部分为50-100个词元）。
- • 层次化文档分块（Hierarchical Document Chunking）：根据词汇边界（如章节、节、段落）拆分文档。
- • 句子分块（Sentence Chunking）：将文档拆分成单独的句子。
- • 语义分块（Semantic Chunking）：将文档拆分成句子，生成嵌入向量，并在嵌入向量之间的距离超过某一阈值时进行拆分。

## **检索模式**

下面内容仅列出了基于对应图结构相关的检索模式，详细检索模式的介绍请访问Retrieval Patterns\[3\]。

| English | 中文 |
| --- | --- |
| Cypher Templates | Cypher 模板 |
| Dynamic Cypher Generation | 动态 Cypher 生成 |
| Global Community Summary Retriever | 全局社区摘要检索器 |
| Graph-Enhanced Vector Search | 图增强向量搜索 |
| Hypothetical Question Retriever | 假设问题检索器 |
| Local Retriever | 本地检索器 |
| Metadata Filtering | 元数据过滤 |
| Parent-Child Retriever | 父子检索器 |
| Pattern Matching | 模式匹配 |
| Text2Cypher | 文本转 Cypher |

## **图谱建模**

下面内容仅列出了内容大纲，详细图结构信息请访问Graph Shapes\[4\]进行阅读。

### **相关概念**

- • Domain graph - 领域图

这个术语通常指的是与某个特定领域（如金融、医疗、教育等）相关的图形结构，用于表示领域中的实体及其相互关系。领域图侧重于展示领域内不同概念或对象之间的联系。

- • Lexical graph - 词汇图

词汇图指的是通过词汇之间的关系（如同义词、反义词、上下位词等）来表示词汇网络的图形结构。它用于捕捉和描述词汇之间的语义关系，常见于自然语言处理和语义网络中。

简单来说，领域图注重特定领域中的知识结构，而词汇图注重词汇和语义的关联。

### **图结构**

- • 主要图结构列表如下：

| English | 中文 |
| --- | --- |
| Domain Graph | 领域图 |
| Lexical Graph | 词汇图 |
| Lexical Graph with Extracted Entities | 包含提取实体的词汇图 |
| Lexical Graph with Extracted Entities and Community Summaries | 包含提取实体和社区摘要的词汇图 |
| Lexical Graph with Hierarchical Structure | 包含层级结构的词汇图 |
| Lexical Graph with Hypothetical Questions | 包含假设问题的词汇图 |
| Parent-Child Lexical Graph | 父子词汇图 |
| Lexical Graph with Sibling Structure | 包含兄弟结构的词汇图 |
| Memory Graph | 记忆图 |
| Text Sequence | 文本序列 |

### **引用链接**

`[1]` TOC: *GraphRAG访问模式和知识图谱建模*  
`[2]` graphrag.com: *[https://github.com/graphrag](https://link.zhihu.com/?target=https%3A//github.com/graphrag)*  
`[3]` Retrieval Patterns: *[https://graphrag.com/reference/graphrag/basic-retriever/](https://link.zhihu.com/?target=https%3A//graphrag.com/reference/graphrag/basic-retriever/)*  
`[4]` Graph Shapes: *[https://graphrag.com/reference/knowledge-graph/domain-graph/](https://link.zhihu.com/?target=https%3A//graphrag.com/reference/knowledge-graph/domain-graph/)*

![[Read It Later/attachments/7f51582543216f6ce09baf09e9a4d172_MD5.jpg]]