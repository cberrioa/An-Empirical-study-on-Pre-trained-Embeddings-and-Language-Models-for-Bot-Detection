# Dataset generation
Although the human and bot twitter account dataset is not longer available from the [original source](https://www.cl.cam.ac.uk/~szuhg2/data/characterisation_processed.zip), it can be found [here](./classification_processed).

We are going to create two datasets, one with tweets made by human accounts, and one with tweets made by bot accounts. To download tweets from Twitter, we are going to use the [twitter API](https://developer.twitter.com/en/docs), and to make things more easily, we are going to use the [Twitter Ruby Gem](https://rdoc.info/gems/twitter). To use this library we need to install [ruby](https://www.ruby-lang.org/en/), [Twitter Ruby Gem](https://rdoc.info/gems/twitter) and the [csv gem](https://github.com/ruby/csv).

Last step before launching the scripts is to get [Twitter Consumer API keys](https://developer.twitter.com/en/docs/basics/authentication/overview/application-only).

So once we have download the twitter human and bot account dataset, installed ruby, and the required ruby gems, and get our Twitter Consumer API keys, we can edit the program-bots.rb and program-humans.rb, set the config.consumer_key and config.consumer_secret variables with your Twitter consumer API keys, and run the scripts with: 

```
ruby program-bots.rb
ruby program-humans.rb
```
Please be aware that the scripts are expecting the "classification_processed" folder to be in the same folder. 

If everything is fine, two CSV files containing human and bot tweets will be generated 'tweets-humans.csv' and 'tweets-bots.csv'.

To preprocess the dataset (substitute url to tags, split words with "/", tag users, tag emoticons and numbers, split hashtags on uppercase, mark puntuation repetitions, mark elongated words, and mark allcaps), use the following commands:
```
ruby preprocess-twitter.rb tweets-humans.csv tweets-humans-preprocessed.csv
ruby preprocess-twitter.rb tweets-bots.csv tweets-bots-preprocessed.csv
```
This preprocess script is in based on the [Ruby script for preprocessing Twitter data](https://nlp.stanford.edu/projects/glove/preprocess-twitter.rb), used to generate the Twitter [GloVe embeddings](https://nlp.stanford.edu/projects/glove/)

We created the training and test datasets joining both human and bot tweet datasest in one dataset, taking a random sample of 500000 tweets for training and 100000 random tweets for testing. The code can be found at [Generate_human_and_bots_tweets_dataset.ipynb](./Generate_human_and_bots_tweets_dataset.ipynb). This notebook can be imported in [Google Colab](https://colab.research.google.com), and can be runned from there if you want. You need to upload the 'tweets-humans.csv' and 'tweets-bots.csv' into Google Drive.
 
 You can use the same notebook to generate the dataset of preprocessed tweets.
