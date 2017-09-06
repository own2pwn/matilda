# Matilda
Matilda is a telegram bot written in Python 3 to scrape news articles, written in order to allow me to get a better understanding of Python. This bot is purely for educational purposes.

Matilda is currently still in the development stage. Currently, I only have time to work on Matilda on the weekends, so development for this bot might be a little slow.

## Supported Sites
* Straits Times
* ChannelNewsAsia

## Licensing
Matilda is licensed under the [Affero General Public License Version 3](LICENSE).

## Sample
A sample version of this bot is currently running on Telegram, under @matilda_jk_bot. 

![Sample Gif](https://thumbs.gfycat.com/PepperyUnrulyHarborseal-size_restricted.gif)

## Credits
* Thanks to [LFlare](https://github.com/LFlare) for giving me the idea, and letting me take a look at his source code when I was stuck.
* [Python-Telegram-Bot](https://github.com/python-telegram-bot/python-telegram-bot) for making a wonderful wrapper, and having an excellent community who are willing to devote time to assist others.

## Contact
You can open an issue here to contact me regarding bugs.

## Commands
* /cmd (full command list)
* /aboutme (about Matilda)
* /supported (supported sites)
* /cna <article> (scrapes CNA Articles)
* /st <article>  (scrapes straits times article)
* /cna_search <terms> (Searches for CNA Articles)
* /cna_new (Latest five CNA Articles)
* /st_search <terms> (Searches for ST Articles)
* /st_new (Latest five ST Articles)
* /st_rand (Randomly generates 5 articles from StraitsTimes)
* /cna_rand (Randomly generates 5 articles from CNA)

## How does Matilda work?
If you have the article url, you can simply run /st or /cna <article url>

If not, you can use the search feature, to either search for specific keywords that appear in the article title, or to get the latest 5 articles.

The reason why only 5 articles are supported is because the sample version of this bot is not running on a very powerful server, and I do not wish to overload it.

From there, you can then use the inline buttons generated by the bot to read the article from the comfort of your telegram chat.

## Usage
Install the following python libraries
* python-telegram-bot
* Beautiful Soup 4
* Requests
* Python String Utilities
* dateutil
* PyMySQL


Setup a MySQL Database. A schema will be provided shortly.
![exampledb](/examples/dbschema_matilda.png)

Update token.py with your bot's api token, mysql information, and the list of user ids for admin.


Start your bot with 
```bash
python3 matilda.py
```


If you are running Matilda on linux, you may also want to use this command to ensure that Matilda keeps running after you exit the terminal.

```bash
sudo nohup python3 matilda.py > /home/matilda-live/error.log 2>&1 &
```
