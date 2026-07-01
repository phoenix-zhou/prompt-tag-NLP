
📚 Recommendation System - Text Tag Classification NLP
--- 
This project implements a complete iteration from traditional machine learning to BERT pre-trained models. By leveraging dynamic quantization and knowledge distillation techniques, it achieves extreme inference acceleration and model lightweighting while maintaining high accuracy (93.64%), making it perfectly suited for high-concurrency online recommendation scenarios.
Download Link for the pytorch_model.bin model in the bert_pretrain folder: https://pan.baidu.com/s/18y5k6p976VLtnEZ1xtNXIQ?pwd=bpvh (Extraction Code: bpvh)
## 📋 Table of Contents
- Project Background
- Core Features & Tech Stack
- Model Evolution & Performance Metrics
- Engineering Implementation: Compression & Acceleration
- Project Achievements
- Environment Dependencies

--- 
## 📖 Project Background
In personalized recommendation systems, the precise distribution of massive amounts of short-text information is key to enhancing user experience. This project led the design and implementation of a Recommendation System - Intelligent Text Classification Engine, serving as a core upstream task for the recommendation system.
- **Pain Point**: Short texts have sparse semantics and high noise levels, making it difficult for traditional keyword matching to meet the demands of precise distribution.
- **Objective**: Automatically classify news and information into channels of user interest (e.g., History, Finance, Beauty, etc.).
- **Value**: Significantly improves Click-Through Rate (CTR), subscription volume, and paid conversion rates.
## 🛠️ Core Features & Tech Stack
This project covers the entire workflow from data cleaning, feature engineering, and baseline model construction to deep learning iteration and model compression/deployment.
### Tech Stack Overview
- **Deep Learning Frameworks**: PyTorch, Transformers (HuggingFace)
- **Pre-trained Models**: BERT (Base/Small)
- **Classic Models**: TextCNN, FastText, Random Forest
- **NLP Technologies**: Jieba Tokenization, TF-IDF, Tokenization, Padding, Masking
- **Optimization Strategies**: AdamW, Cross Entropy Loss, Learning Rate Warmup
- **Model Compression**: Dynamic Quantization (INT8), Knowledge Distillation
---  
## Model Evolution & Performance Metrics
This project led the complete iteration path of the model from traditional machine learning to SOTA pre-trained models, achieving a leap in classification accuracy.

| Stage | Model Architecture | Key Technologies | Accuracy |
| :--- | :--- | :--- | :--- |
| Baseline | Random Forest | TF-IDF Feature Extraction + Stop Word Filtering | 81.20% |
| Iteration | FastText | N-gram Features + Automated Hyperparameter Tuning (Autotune) | 91.73% |
| SOTA | BERT | Native PyTorch Implementation + In-depth Error Analysis (Badcase) | 93.64% |

**Note**: The BERT model achieved the best business results by encapsulating a standardized data processing pipeline (DatasetIterater) and a complete training loop.
--- 
## ⚡ Engineering Implementation: Compression & Acceleration
To address inference latency bottlenecks in high-concurrency online scenarios, this project led the model lightweighting initiative, achieving a "perfect balance between accuracy and performance."
### 1. Dynamic Quantization
Dynamic quantization was applied to the BERT model using torch.qint8.
- **Effect**: The model file size was reduced by 256.6MB.
- **Performance**: The F1-score was maintained at 91.92% (a minor drop of 1.72%).
- **Benefit**: Significantly reduced GPU memory usage and improved inference throughput.
### 2. Knowledge Distillation
A BERT (Teacher) ➡️ TextCNN (Student) distillation scheme was designed and implemented.
- **Compression Ratio**: The model size was compressed from 409.2MB to 23.1MB (a 17.7x reduction).
- **Accuracy Retention**: The test set accuracy was maintained at 91.25% (a drop of only 2.39%).
- **Conclusion**: Perfectly balances high accuracy with low latency, suitable for deployment in edge or ultra-fast response scenarios.
---
## 🏆 Project Achievements
1. **Business Metric Improvement:**
   - Successfully embedded the engine into the core pipeline of the recommendation system, enabling automated distribution of massive information.
   - Effectively increased CTR, subscription volume, and paid conversion rates for target channels.
2. **Technical Breakthroughs:**
   - Solved the problems of difficult short-text classification and slow inference.
   - Established a standardized NLP model training and compression pipeline, providing an engineering template for subsequent NLP tasks.
## 💻 Environment Dependencies
```
python >= 3.8
torch >= 1.10.0
transformers >= 4.15.0
scikit-learn
jieba
numpy
pandas
```
---
### 📄 License
This project is for learning and communication purposes only.
For detailed project steps, please refer to the blog post:
```
https://blog.csdn.net/zhoupenghui168/article/details/161697018
```
------------------------------------------------------------------------------------------
推荐系统-文本标签分类NLP

---

本项目实现了从传统机器学习到 BERT 预训练模型的完整迭代，并通过动态量化与知识蒸馏技术，在保障高准确率（93.64%）的同时，实现了极致的推理加速与模型轻量化，完美适配线上高并发推荐场景。
bert_pretrain文件夹下面的pytorch_model.bin模型下载地址:  https://pan.baidu.com/s/18y5k6p976VLtnEZ1xtNXIQ?pwd=bpvh 提取码: bpvh

## 📋 目录

- 项目背景
- 核心特性与技术栈
- 模型演进与性能指标
- 工程化落地：压缩与加速
- 项目业绩
- 环境依赖

---

## 📖 项目背景

在个性化推荐系统中，海量短文本资讯的精准分发是提升用户体验的关键。本项目主导设计并落地了**推荐系统-文本智能分类引擎**，将其作为推荐系统的核心前置子任务。

- **痛点**：短文本语义稀疏、噪声大，传统关键词匹配难以满足精准分发需求。
- **目标**：将资讯自动分类至用户感兴趣的频道（如历史、财经、美妆等）。
- **价值**：显著提升点击量（CTR）、订阅量与付费转化率。

---

## 🛠️ 核心特性与技术栈

本项目涵盖了从数据清洗、特征工程、基线模型构建、深度学习迭代到模型压缩部署的全流程。

### 技术栈概览

- **深度学习框架**: PyTorch, Transformers (HuggingFace)
- **预训练模型**: BERT (Base/Small)
- **经典模型**: TextCNN, FastText, Random Forest
- **NLP 技术**: Jieba分词, TF-IDF, Tokenization, Padding, Masking
- **优化策略**: AdamW, Cross Entropy Loss, Learning Rate Warmup
- **模型压缩**: **Dynamic Quantization (INT8)**, **Knowledge Distillation**

---

## 📈 模型演进与性能指标

本项目主导了模型从传统机器学习到 SOTA 预训练模型的完整迭代路径，分类准确率实现跨越式增长。

| 阶段 | 模型架构 | 关键技术点 | 准确率 (Accuracy) |
| ------ |------ |------ |------ |
| **Baseline** | Random Forest | TF-IDF 特征提取 + 停用词过滤 | **81.20%** |
| **Iteration** | FastText | N-gram 特征 + 自动化超参寻优 (Autotune) | **91.73%** |
| **SOTA** | **BERT** | PyTorch 原生搭建 + 深度错误分析 (Badcase) | **93.64%** |

**注**：BERT 模型通过封装标准化的数据处理管道（DatasetIterater）与完整的训练闭环，实现了最佳的业务效果。

---

## ⚡ 工程化落地：压缩与加速

针对线上高并发场景的推理延迟瓶颈，本项目主导了模型轻量化改造，实现了“精度与性能的完美平衡”。

### 1. 动态量化

采用 `torch.qint8` 对 BERT 模型进行动态量化。

- **效果**：模型文件大小缩减 **256.6MB**。
- **性能**：F1-score 保持在 **91.92%**（仅微降 1.72%）。
- **收益**：大幅降低显存占用，显著提升推理吞吐量。

### 2. 知识蒸馏

设计并落地了 **BERT (Teacher) ➡️ TextCNN (Student)** 的蒸馏方案。

- **压缩比**：模型体积从 **409.2MB** 压缩至 **23.1MB**（缩减 **17.7倍**）。
- **精度保持**：测试集准确率保持在 **91.25%**（仅下降 2.39%）。
- **结论**：完美兼顾了高精度与低延迟，适合边缘侧或极速响应场景部署。

---

## 🏆 项目业绩

1. **业务指标提升**：
    - 成功将引擎内嵌至推荐系统核心链路，实现海量资讯自动化分发。
    - 有效提升了目标频道的 **CTR**、**订阅量**与**付费转化率**。
2. **技术突破**：
    - 解决了短文本分类难、推理慢的问题。
    - 建立了标准化的 NLP 模型训练与压缩 Pipeline，为后续其他 NLP 任务提供了工程范本。

---

## 💻 环境依赖

```
python >= 3.8
torch >= 1.10.0
transformers >= 4.15.0
scikit-learn
jieba
numpy
pandas
```

---

### 📄 License

本项目仅供学习与交流使用。
项目具体步骤见博客:
```
https://blog.csdn.net/zhoupenghui168/article/details/161697018
```

