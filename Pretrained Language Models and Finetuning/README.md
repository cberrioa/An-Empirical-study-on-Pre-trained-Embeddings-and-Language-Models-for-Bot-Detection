# How to finetune BERT?
We used the [code](https://github.com/google-research/bert) provided by Google to [finetune](https://github.com/google-research/bert#sentence-and-sentence-pair-classification-tasks) the [BERT-Base, Uncased](https://storage.googleapis.com/bert_models/2018_10_18/uncased_L-12_H-768_A-12.zip) model, and trained our Bot or Human classifier. 
We had to adapt our datasest to be able to uses the run_classifier.py script, as task_name we used COLA. 
Once BERT is finetuned and trained, we can use the finetuned model to predict the test dataset labels and do the [evaluation](./BERT-results.ipynb). 

# How to finetune OpenAI's GPT model?
We used the [PyTorch implementation of OpenAI's Finetuned Transformer Language Model for classification task](https://github.com/tingkai-zhang/pytorch-openai-transformer_clas/) which is based on [PyTorch implementation of OpenAI's Finetuned Transformer Language Model](https://github.com/huggingface/pytorch-openai-transformer-lm). 
We also had to adapt our dataset to the SST2 dataset format. Please find the evaluation results in [open-ai-results.ipynb](./open-ai-results.ipynb)

# How to finetune the Universal Language Model (ULMFit)?
We used the [fastai library](https://docs.fast.ai/index.html) and we followed the [Training an IMDb sentiment model with ULMFiT](https://docs.fast.ai/text.html#Quick-Start:-Training-an-IMDb-sentiment-model-with-ULMFiT) using our dataset. You can find the notebook for the preprocessed dataset in [ULMFit.ipynb](./ULMFit.ipynb)
