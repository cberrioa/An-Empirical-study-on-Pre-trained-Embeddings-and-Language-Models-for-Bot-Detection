This folder includes code to train a BiLSTM using random trainable (dynamic) and ELMO embeddings. ELMO embeddings are contextualized 
embeddings, therefore a word has a different embedding in a different sentence. In order to avoid creating these embeddings multiple 
times (we used 10-fold cross validation), first we get the embeddings of each word for each sentence of the dataset, and we save the 
these embeddings in a hdf5 file. These embeddings are stored in a way that they can be accesed in a easy way, so when we need the 
ELMO emeddings for a sentence, we get them from the file. Please find the code to create this embeddings file for the whole dataset 
of preprocessed tweets in [ELMO-embeddings-preprocessed.ipynb](./CNN-based%20notebooks/ELMO-embeddings-preprocessed.ipynb). This file will be required to execute the experiment in 
 	[BiLSTM ELMO+Random.ipynb](./Bi-LSTM%20notebooks/BiLSTM%20ELMO+Random.ipynb).