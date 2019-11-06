# Dataset generation
Although the human and bot twitter account dataset is not longer available from the [original source](https://www.cl.cam.ac.uk/~szuhg2/data/characterisation_processed.zip), it can be found [here](https://github.com/Flajt/Twitter_bot_detection/tree/ml-model/Datasets/classification_processed).

We are going to create two datasets, one with tweets made by human accounts, and one with tweets made by bot accounts. To download tweets from Twitter, we are going to use the [twitter API](https://developer.twitter.com/en/docs), and to make things more easily, we are going to use the [Twitter Ruby Gem](https://rdoc.info/gems/twitter). To use this library we need to install [ruby](https://www.ruby-lang.org/en/), [Twitter Ruby Gem](https://rdoc.info/gems/twitter) and the (csv gem)[https://github.com/ruby/csv].

Last step before launching the scripts is to get [Twitter Consumer API keys](https://developer.twitter.com/en/docs/basics/authentication/overview/application-only).

So once we have download the twitter human and bot account dataset, installed ruby, and the required ruby gems, and get our Twitter Consumer API keys, we can edit the program-bots.rb and program-humans.rb, set the config.consumer_key and config.consumer_secret variables with your Twitter consumer API keys, and run the scripts with: 

```
ruby program-bots.rb
ruby program-humans.rb
```
Please be aware that the scripts are expecting the "classification_processed" folder to be in the same folder. Just copy the folder to the same folder, or modify the script to read the "classifcation_processed" where is located.

If everything is fine, two CSV files containing human and bot tweets will be generated 'tweets-humans.csv' and 'tweets-bots.csv'.
