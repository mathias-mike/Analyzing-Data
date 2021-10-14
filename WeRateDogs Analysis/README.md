# WeRateDogs twitter data analysis
WeRateDog is a twitter user with the handle @dog_rates that gives dogs great ratings beacuase [they are good dogs brant](https://knowyourmeme.com/memes/theyre-good-dogs-brent). The project was majored around the wrangling part of the data analysis process and so most of the work done was wrangling (well, I have also leanrt and seen first hand that this part of the data analyst life is quite time consuming but fun at the same time)

Below are what I did to gather the data;
## Gathering
I started off my wrangling process by downloading the `twitter_archive_enhanced.csv` from the udacity classroom and then I read in the file into a `pandas.DataFrame` I called `df_archive`.

Next I used the `requests` library to request for the file stored in the udacity server as [image-predictions.tsv](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv). I initialized a cursor on the `response.text` at position zero with `io.StringIO()` and read this into a `pandas.DataFrame` I called `df_ipred`.

And lastly I queried the twitter API using the `tweepy` twitter access library to fectch *retweet_counts* and *favorite_counts*. First of, I needed to create a developer account on twitter and get it approved (fortunately this was a success for me) and then I got keys and tokens that grants me access to the API. I stored the data I got from twitter in a file called `tweet_json.txt` from where I read in the tweet *retweet_counts* and *favorite_counts* into a `pandas.DataFrame` called `df_rt_fav`.

## Accesssing
In accessing the 3 dataset gathered, I found and cleaned the following quality and tidiness issues;
### Quality issues
#### df_archive
* Missing values (in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp, expanded_urls).

* Multiple values in expanded_url.

* HTML tags in source

* Erroneous datatypes (tweet_id, timestamp, source)

* Incorrect rates (e.g, 75/10 instead of 9.75/10...)

* Incorrect dog names (a, such, quite None...)

* None in columns name, doggo, floofer, pupper and puppo.

#### df_rt_fav
* Erroneous datatypes (tweet_id)

#### df_ipred
* Erroneous datatypes (tweet_id)

* Non descriptive column names (p1, p1_conf, p1_dog, p2, p2_conf, p2_dog, p3, p3_conf, p3_dog)

### Tidiness issues
* doggo, floofer, pupper and puppo should be under one variable name dog_stage.

* Merge df_rt_fav with df_archive.

* Same variables split to different columns (p1, p2, p3), (p1_conf, p2_conf, p3_conf), (p1_dog, p2_dog, p3_dog).

Feel free to view the [wrangle_act.ipynb](https://github.com/mathias-mike/Analyzing-Data/blob/master/WeRateDogs%20Analysis/wrangle_act.ipynb) notebook file for a full overview of the project. The notebook file contains wrangling acts done to get the data from dirty to clean and interesting insight garnered from an analysis of the dataset.
