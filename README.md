# Suggested Tweet Tag

A [Liquid tag](http://wiki.shopify.com/Liquid) for [Jekyll](http://jekyllrb.com/) that allows for the embedding of suggested tweets via [Twitter’s Web Intents API](https://dev.twitter.com/docs/intents).

* __Authors:__ David Ensinger and John Colvin
* __Site:__ [http://davidensinger.com/](http://davidensinger.com/) and [http://2john4tv.biz/](http://2john4tv.biz/)
* __Twitter:__ [@DavidEnsinger](https://twitter.com/intent/user?screen_name=DavidEnsinger) and [@2john4tv](https://twitter.com/intent/user?screen_name=2john4tv)
* __Email:__ hello@davidensinger.com and 2john4tv@gmail.com
* __Source:__ [https://github.com/davidensinger/suggested-tweet](https://github.com/davidensinger/suggested-tweet)

(John did all wranglin’ of Rich’s code. I just bought him pizza and told him what I wanted.)

## Big Thanks

This plugin is based upon [Rich Hollis’s](https://github.com/richhollis) [Twitter Web Intents Ruby Gem](https://github.com/richhollis/twitter_web_intents).
* __Source:__ [https://github.com/richhollis/twitter_web_intents](https://github.com/richhollis/twitter_web_intents)

Please note that you’ll need to install the Twitter Web Intents gem as it’s required.

## Installation

1. Copy **suggested-tweet.rb** into your site’s **_plugins** directory
2. Install **twitter_web_intents gem**, either manually or via **Bundler**
3. Add desired parameters (see [Configuration](#configuration)) to **_config.yml**
4. Add desired parameters to **YAML front-matter** of page
5. Add `{% suggested_tweet %}` tag to your post or template.

## Configuration

The following parameters may be set globally in **_config.yml** or on a per page basis in the **YAML front-matter**. Parameters set in the **YAML front-matter** take precedence over those set in **_config.yml**. Note that all parameters are optional.

```
suggested_tweet:
  url:                  'http://davidensinger.com/'
  via:                  'davidensinger'
  text:                 'Hello world'
  in_reply_to:          331434728957833218
  hashtags:             ['Jekyll', 'Twitter']
  related:              ['davidensinger', 'richhollis', '2john4tv']
```

## Usage

`{% suggested_tweet %}`

## Output

`https://twitter.com/intent/tweet?hashtags=Jekyll,Twitter&in_reply_to=331434728957833218&related=davidensinger,richhollis,2john4tv&text=Hello+world&url=http%3A%2F%2Fdavidensinger.com&via=davidensinger`

## Liquid Output for Parameters

As an example we’ll use the text parameter:

- **_config.yml:** `{{ site.suggested_tweet.text }}`
- **YAML front matter:** `{{ page.suggested_tweet.text }}`

## Todo

* Add option to combine parameters set in both **_config.yml** and **YAML front-matter** of page, i.e. `hashtags` and `related`.

## Contribute

Please do!
