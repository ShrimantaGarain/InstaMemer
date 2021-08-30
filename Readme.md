# Instamemexbot


## About
**Instamemexbot** is bot which automatically post Memes and Facts on Instagram . The bot posts top Memes from Reddit pages. Bot also post amazing facts and photographs linked with a keyword from the facts.


## How it works and what it does?
➡️ For Memes, It uses the PRAW – Python Reddit API Wrapper and fetches Memes Images from the different [Reddit](https://www.reddit.com/) Pages.

➡️ On fectching Meme image from reddit, using Pillow library the image is edited to make image ratio 1.0 and watermark is added at top right corner. As the editing is complete it saves the image and is then posted on Instagram using [Instabot](https://pypi.org/project/instabot/) package.

➡️ For facts, It uses the [Random useless facts API](https://uselessfacts.jsph.pl/)

➡️ On fetching the fact it is parsed through [Rapid Automatic Keyword Extraction algorithm](https://github.com/csurfer/rake-nltk) (Rake-nltk) which gives a keyword from the fact . The extracted keyword is then passed to unsplash api for searching that relevant picture for the fact. 

➡️ After receiveing all the metrics and image, using Pillow library the image is edited with the fact and a watermark. As the editing process is complete it saves the image and is then posted on Instagram using [Instabot](https://pypi.org/project/instabot/) package.

➡️ The bot is deployed via Heroku and scheduled to run at intervals using Herokuscheduler.

## Architecture
```
├── LICENSE
├── Procfile
├── README.md
├── .fonts
│   └── Ts.ttf
├── listofpages.txt
├── requirements.txt
├── nltk.txt
├── runtime.txt
├── randmness_checker.py
├── fact.py
├── meme.py
├── main.py
```

### Requirements
- instabot
- Rake-nltk
- Urllib3
- Pillow
- resizeimage
- Python==3.6
- Reddit API, Unsplash API, Useless facts API


 > If you want to run it locally
 ```
 git clone https://github.com/marclave/InstaBot.git
 ```
 >run the following command to install the required libraries:
 ```
 pip install -r requirements.txt
 ```

 >add your Instagram creadentials, Unsplash keys 🔑 in fact.py and Reddit keys 🔑 in meme.py. To run the bot first you have to change Time in main.py after changing time run     following command in command prompt
 ```
 python main.py
 ```
 >If you are using any IDE then run main.py


</a><br>

