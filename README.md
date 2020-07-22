# EconoTW Retweet Bot
This python personal retweet bot using Tweepy searches and retweets based on hashtags #econotw or #EconTwitter and also a given list of users. Can be fastly addapted to multiple keywords, or hashtags, and to favorite tweets before retweeting.

This script bot is designed to run indefinitely even if exceptions do occur. Consider submiting your modifyed version at an external server, raspberry pi, or equivalents.

You can see this bot working at [econotw](https://twitter.com/econotw).

Requirements
----------

`tweepy==3.8.0`

`tdqm==4.47.0`

Usage
----------

First of all, you need to add your Twitter API keys in `keys.py`script file.

A simple function is designed to call the econotwbot objetc with it's key args.

```
play(test=False)
```

I had choose this way becouse I don't want the script to stop by **any** reason. You can aways call the econotwbot object in your own rules.

If you want to retweet specific users, add then in the `to_follow.txt` file.

This bot is designed to work in 30 minutes intervals, with more intervals between tasks to avoid overloading your API. You can configure how many retweets you want to retrive from each user from `to_follow.txt` using the parameter `i_pages`, and your last querys using `i_hashtag`. 

Also, you can choose to like the tweets before retweet then setting `like_pages=True` or  `like_hashtag=True`, but I do not encourage this behaviour becouse it consumes a lot of the free branch API.

By default:

`play(test=True,i_pages=3, i_hashtag=20, like_pages=False, like_hashtag=False)`

## To-do's

- This code is still bad documented. Besides the code being quite self explanatory this must be done (when I have the courage).
- I'm also considering to add an e-mail module to alert the admin in case of unhandled exceptions.

