# An Empirical study on Pre-trained Embeddings and Language Models for Bot Detection.

## Motivation
**While word embeddings are learnt from large corpora, their use in neural models to solve specific tasks is limited to the input layer.** So in practice a task-specific neural model is built almost from scratch because most of the model parameters are initialized randomly, and hence, these paremeters need to be optimized for the task at hand, requiring large sets of data to produce a high performance model.

**Recent advances in neural language models** (BERT or OPEN AI GPT) have shown evidence that task specific architectures are not longer necessary and transfering some internal representations (attention blocks) along with shallow feed forward networks is enough. 

**In (Garcia et al.,2019) we presented an experimental study** on the use of word embeddings as input of CNN architectures and Bi-LSTM to tackle the bot detection task and compare these results with fine-tuning pretrained language models. 

**Evaluation results, presented in the figure below, show that fine-tuning language models yields overall better results than training specific neural architectures** that are fed with mixture of: i) pre-trained contextualized word embeddings (ELMo), ii) pre-trained  context-indepedent word embeddings learnt from Common Crawl(FastText), Twitter (GloVe), and urban dictionary (word2vec), plus embeddings optimized by the neural network in the learning process. 

![Bot detection classification task](https://drive.google.com/uc?id=1rSzM544MK2QOezpvUKHfrxATbkEiyBHX)

## Dataset generation
Please find the required code to generate the human-or-bot dataset in [dataset generation](./dataset%20generation).
Dataset generation can be a little bit time consuming, if you want to get the datasets, please send us an email <agarcia@expertsystem.com>, <cberrio@expertsystem.com> or <jmgomez@expertsystem.com>.

## CNN and BiLSTM experiments
Since there were many experiments in the paper, only will be uploaded the code of those with the best results. Please feel free to ask for the other experiments.

## References

Garcia-Silva, Andres, et al. "An Empirical Study on Pre-trained Embeddings and Language Models for Bot Detection." Proceedings of the 4th Workshop on Representation Learning for NLP (RepL4NLP-2019). 2019.

To cite this paper use the following BibTex entry: 

```
@inproceedings{garcia-silva-etal-2019-empirical,
    title = "An Empirical Study on Pre-trained Embeddings and Language Models for Bot Detection",
    author = "Garcia-Silva, Andres  and
      Berrio, Cristian  and
      G{\'o}mez-P{\'e}rez, Jos{\'e} Manuel",
    booktitle = "Proceedings of the 4th Workshop on Representation Learning for NLP (RepL4NLP-2019)",
    month = aug,
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/W19-4317",
    doi = "10.18653/v1/W19-4317",
    pages = "148--155",
}
```
