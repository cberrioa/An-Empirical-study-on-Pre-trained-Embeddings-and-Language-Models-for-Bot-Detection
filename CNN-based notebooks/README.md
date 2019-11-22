# CNN experiments
This folder incluides code to train a CNN using random trainable (dynamic) and ELMO embeddings. ELMO embeddings are contextualized embeddings,
therefore a word has a different embedding in a different sentence. In order to avoid creating these embeddings multiple times,
we get the embeddings for the whole dataset, and use generator to get the embeddings for a particular sentence. Please find the code to get 
the embeddings for the whole dataset of preprocessed tweets in [ELMO preprocessed embeddings](./CNN-based%20notebooks/ELMO-embeddings-preprocessed.ipynb).
These dataset with embeddings are used in [CNN Dynamic ELMO notebook](./CNN-based%20notebooks/CNN%20Dynamic+ELMO.ipynb).
