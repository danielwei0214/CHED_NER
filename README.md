### CHED_NER 数据集描述

CHED_NER 数据集是古汉语历史事件检测数据集 (CHED) 转换格式后的子集，将事件检测任务建模为序列标注任务，专门用于命名实体识别 (NER) 任务。该数据集采用 BIO（Begin, Inside, Outside）格式，其中每个词被标注为事件触发词（B-标签）、触发词的一部分（I-标签），或者非事件相关的词（O）。这种格式非常适合用于序列标注模型的训练和评估。

### 数据集结构

- **train.txt**: 包含训练数据，格式为 BIO 词汇分类格式。每行表示一个词汇及其对应的标签（B、I 或 O）。
- **dev.txt**: 包含开发/验证数据，用于在训练过程中调整和验证模型性能。
- **test.txt**: 包含测试数据，用于评估最终模型的性能。

### 数据集格式示例

数据集中的每一行都以“词汇 标签”的形式呈现，其中标签为 B-事件类型、I-事件类型或 O。例如：

```
寻 O
以 O
本 O
官 O
行 B-职位-官位-任职
梁 O
州 O
刺史 O
。 O
```

### 用途

CHED_NER 数据集主要用于训练和评估基于序列标注的事件检测模型。它将古代汉语文本中的事件检测问题转化为一个命名实体识别 (NER) 问题，适合于开发和测试用于古文历史文本事件检测的自然语言处理模型。该数据集可以从 GitHub 仓库获取：[CHED GitHub](https://github.com/lcclab-blcu/CHED)。

### 引用

如果您在研究中使用了该数据集，请引用以下论文：

```bibtex
@inproceedings{congcong-etal-2023-ched,
    title = "{CHED}: A Cross-Historical Dataset with a Logical Event Schema for Classical {C}hinese Event Detection",
    author = "Congcong, Wei  and
      Zhenbing, Feng  and
      Shutan, Huang  and
      Wei, Li  and
      Yanqiu, Shao",
    editor = "Sun, Maosong  and
      Qin, Bing  and
      Qiu, Xipeng  and
      Jiang, Jing  and
      Han, Xianpei",
    booktitle = "Proceedings of the 22nd Chinese National Conference on Computational Linguistics",
    month = aug,
    year = "2023",
    address = "Harbin, China",
    publisher = "Chinese Information Processing Society of China",
    url = "https://aclanthology.org/2023.ccl-1.74",
    pages = "875--888",
    abstract = "{``}Event detection (ED) is a crucial area of natural language processing that automates the extrac-tion of specific event types from large-scale text, and studying historical ED in classical Chinesetexts helps preserve and inherit historical and cultural heritage by extracting valuable informa-tion. However, classical Chinese language characteristics, such as ambiguous word classes andcomplex semantics, have posed challenges and led to a lack of datasets and limited research onevent schema construction. In addition, large-scale datasets in English and modern Chinese arenot directly applicable to historical ED in classical Chinese. To address these issues, we con-structed a logical event schema for classical Chinese historical texts and annotated the resultingdataset, which is called classical Chinese Historical Event Dataset (CHED). The main challengesin our work on classical Chinese historical ED are accurately identifying and classifying eventswithin cultural and linguistic contexts and addressing ambiguity resulting from multiple mean-ings of words in historical texts. Therefore, we have developed a set of annotation guidelinesand provided annotators with an objective reference translation. The average Kappa coefficientafter multiple cross-validation is 68.49{\%}, indicating high quality and consistency. We conductedvarious tasks and comparative experiments on established baseline models for historical ED inclassical Chinese. The results showed that BERT+CRF had the best performance on sequencelabeling task, with an f1-score of 76.10{\%}, indicating potential for further improvement. 1Introduction{''}",
    language = "English",
}
```

有关更多详情，请参考上述 GitHub 仓库。

---

### CHED_NER Dataset Description

The CHED_NER dataset is a subset of the Classical Chinese Historical Event Detection (CHED) dataset, reformatted for named entity recognition (NER). It models the event detection task as a sequence labeling problem, using the BIO (Begin, Inside, Outside) format. Each word is tagged as an event trigger word (B-tag), part of a trigger word (I-tag), or non-event-related (O). This format is well-suited for training and evaluating sequence labeling models.

### Dataset Structure

- **train.txt**: Contains the training data in BIO token classification format. Each line represents a token and its corresponding label (B, I, or O).
- **dev.txt**: Contains the development/validation data used for tuning and validating model performance during training.
- **test.txt**: Contains the test data used for evaluating the final model's performance.

### Example Format

Each line in the dataset is presented in the format "Token Label," where the label is B-EventType, I-EventType, or O. For example:

```
寻 O
以 O
本 O
官 O
行 B-职位-官位-任职
梁 O
州 O
刺史 O
。 O
```

### Usage

The CHED_NER dataset is primarily used for training and evaluating sequence labeling-based event detection models. It converts the problem of event detection in classical Chinese texts into a Named Entity Recognition (NER) problem, making it suitable for developing and testing natural language processing models for historical text event detection. The dataset can be accessed from the GitHub repository: [CHED GitHub](https://github.com/lcclab-blcu/CHED).

### Citation

If you use this dataset in your research, please cite the following paper:

```bibtex
@inproceedings{congcong-etal-2023-ched,
    title = "{CHED}: A Cross-Historical Dataset with a Logical Event Schema for Classical {C}hinese Event Detection",
    author = "Congcong, Wei  and
      Zhenbing, Feng  and
      Shutan, Huang  and
      Wei, Li  and
      Yanqiu, Shao",
    editor = "Sun, Maosong  and
      Qin, Bing  and
      Qiu, Xipeng  and
      Jiang, Jing  and
      Han, Xianpei",
    booktitle = "Proceedings of the 22nd Chinese National Conference on Computational Linguistics",
    month = aug,
    year = "2023",
    address = "Harbin, China",
    publisher = "Chinese Information Processing Society of China",
    url = "https://aclanthology.org/2023.ccl-1.74",
    pages = "875--888",
    abstract = "{``}Event detection (ED) is a crucial area of natural language processing that automates the extrac-tion of specific event types from large-scale text, and studying historical ED in classical Chinesetexts helps preserve and inherit historical and cultural heritage by extracting valuable informa-tion. However, classical Chinese language characteristics, such as ambiguous word classes andcomplex semantics, have posed challenges and led to a lack of datasets and limited research onevent schema construction. In addition, large-scale datasets in English and modern Chinese arenot directly applicable to historical ED in classical Chinese. To address these issues, we con-structed a logical event schema for classical Chinese historical texts and annotated the resultingdataset, which is called classical Chinese Historical Event Dataset (CHED). The main challengesin our work on classical Chinese historical ED are accurately identifying and classifying eventswithin cultural and linguistic contexts and addressing ambiguity resulting from multiple mean-ings of words in historical texts. Therefore, we have developed a set of annotation guidelinesand provided annotators with an objective reference translation. The average Kappa coefficientafter multiple cross-validation is 68.49{\%}, indicating high quality and consistency. We conductedvarious tasks and comparative experiments on established baseline models for historical ED inclassical Chinese. The results showed that BERT+CRF had the best performance on sequencelabeling task, with an f1-score of 76.10{\%}, indicating potential for further improvement. 1Introduction{''}",
    language = "English",
}
```

For more details, please refer to the GitHub repository mentioned above.
