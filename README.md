# friendly-memory

This is a simple project that let's everyone know about what's happing aroud the world

By sending the top tending news from the most popular media outlets around the world, directly to user's WhatsApp

This project uses [twilio](https://www.twilio.com/console/sms/whatsapp/sandbox) for sending whatapp messages

It will Scrape the most recent articles from any news-site and stores in ``` scraped_articles.json ``` for furter use

Automation in process to send news articles every 6 hours

## How to install
```
git clone git@github.com:manisaiprasad/friendly-memory.git
cd friendly-memory
pip install -r requirements.txt
```

## Now Run

Before Running make sure to edit the twilio credentials

```
python newsscraper.py NewsPapers.json
```
### Configure News Outlets at ```NewsPapers.json```
Add RSS link or news outlet link to ```NewsPapers.json``` like this configuration shown here
```
{
  "bbc": {
    "rss": "http://feeds.bbci.co.uk/news/rss.xml",
    "link": "http://www.bbc.com/"
  },
  "cnn": {
    "rss": "http://rss.cnn.com/rss/edition.rss",
    "link": "http://edition.cnn.com/"
  },
  "foxnews": {
    "rss": "http://feeds.foxnews.com/foxnews/latest",
    "link": "http://www.foxnews.com/"
  },
  "nytimes_international": {
    "link": "https://nytimes.com/",
    "rss": "https://rss.nytimes.com/services/xml/rss/nyt/World.xml"
  },
  "theguardian": {
    "rss": "https://www.theguardian.com/uk/rss",
    "link": "https://www.theguardian.com/international"
  },
  "washingtonpost": {
    "rss": "http://feeds.washingtonpost.com/rss/world",
    "link": "https://www.washingtonpost.com/"
  }
}
```
