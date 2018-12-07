# Songs-Lyrics-Web-Scraper
This is a python script that can scrape lyrics of all the songs by any artist from the web.

# Description

The project has two files :

1. **Songs Names Scraper.ipynb** - This is responsible for creating a json file (**Artists-Songs Mapping.json**) that would have mapping from artist's name to all its available songs. http://www.song-list.net is used to scrape the songs list.

The artists for which the songs list need to be generated are specified in the artists array :
```
# artists list whose songs list is to be made
artists = ["edsheeran", "eminem", "taylorswift", "linkinpark", "drake-2"]
```
Add or remove artists in this array to get the required songs list.



2. **Lyrics Scraper.ipynb** - This is responsible for actually fetching (scraping) the lyrics of all songs (specified in Artists-Songs Mapping.json) by a particular artist from web. https://www.azlyrics.com is used to scrape the lyrics.

Specify the artist in the code for which lyrics need to be scraped :
```
# artist for which the lyrics need to be written
artist = "eminem"
songs = songs_dict[artist]
processed_songs = []
```

Lyrics are saved in **lyrics_scraped.txt**

# Note

While scraping the web, keep in mind to not just make numerous requests to a website continuosly. It may be entirely possible to overburden the website's servers or you might get blocked, preventing further scraping. Try to scrape the content from web in a way as close as possible to how a normal user would copy and paste, in terms of the time required to gather this content. 

To reinforce this, a delay is setup in the code that **waits for 10 seconds** after fetching one lyric.
