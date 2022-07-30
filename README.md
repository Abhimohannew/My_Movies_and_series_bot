# Modified Version Of [Media Search bot](https://github.com/Mahesh0253/Media-Search-bot)

## Added Features
* Imdb posters for autofilter.
* Custom captions for your files.
* Index command to index all the files in a given channel (No USER_SESSION Required).
* Ability to Index Public Channels without being admin.
* Support Auto-Filter (Both in PM and in Groups)
* Once files saved in Database , exists until you manually deletes. (No Worry if post gets deleted from source channel.)
* Added Force subscribe (Only channel subscribes can use the bot)
* Ability to restrict groups(AUTH_GROUPS)

## Installation

### Easy Way
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/subinps/Media-Search-bot)

## Deploy to Railway
<p><a href=https://github.com/abhimohan-tech/Media-Search-bot> <img src="https://img.shields.io/badge/Deploy%20To%20Railway-blueviolet?style=for-the-badge&logo=railway" width="200""/></a></p>

  
<p><a href=https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2Fabhimohan-tech%2FMedia-Search-bot&envs=API_ID%2CAPI_HASH%2CCHANNELS%2CBOT_TOKEN%2CDATABASE_NAME%2CAUTH_CHANNEL%2CAUTH_USERS%2CADMINS%2CSTART_MSG%2CUSE_CAPTION_FILTER%2COMDB_API_KEY%2CCUSTOM_FILE_CAPTION%2CAUTH_GROUPS%2CCOLLECTION_NAME%2CCACHE_TIME%2CDATABASE_URI&optionalEnvs=AUTH_CHANNEL%2CADMINS%2CAUTH_USERS%2CFORCES_SUB%2CSTART_MSG&API_IDDesc=Get+From+my.telegram.org&API_HASHDesc=Get+from+my.telegram.org&BOT_TOKENDesc=Get+from%40Botfather&USE_CAPTION_FILTEResc=ID+of+Channel%2FGroup+where+the+bot+plays+Music.&OMDB_API_KEYDesc=Pyrogram+string+session+of+a+user+account&CUSTOM_FILE_CAPTIONDesc=Group+to+send+Playlist%2C+if+CHAT+is+a+Group%28%29&ADMINSDesc=+ID+of+users+who+can+use+admin+commands.&AUTH_USERSDesc=This+will+be+streamed+on+startups+and+restarts+of+bot.+You+can+use+either+any+STREAM_URL+or+a+direct+link+of+any+video+or+a+Youtube+Live+link.+You+can+also+use+YouTube+Playlist.Find+a+Telegram+Link+for+your+playlist+from+%40DumpPlaylist+or+get+a+PlayList+from++%40GetPlaylistBot.+&FORCES_SUBDesc=A+reply+to+those+who+message+the+USER+account+in+PM.+Leave+it+blank+if+you+do+not+need+this+feature.&START_MSGDesc=Pass+Y+If+you+want+to+make+%2Fplay+command+only+for+admins+of+CHAT.+By+default+%2Fplay+is+available+for+all&referralCode=abhimohannew> <img src="https://img.shields.io/badge/Deploy%20To%20Railway-blueviolet?style=for-the-badge&logo=railway" width="200""/></a></p>

### Hard Way

```bash
# Create virtual environment
python3 -m venv env

# Activate virtual environment
env\Scripts\activate.bat # For Windows
source env/bin/activate # For Linux or MacOS

# Install Packages
pip3 install -r requirements.txt

# Edit info.py with variables as given below then run bot
python3 bot.py
```
Check [`sample_info.py`](sample_info.py) before editing [`info.py`](info.py) file

## Variables

### Required Variables
* `BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.
* `API_ID`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `API_HASH`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `CHANNELS`: Username or ID of channel or group. Separate multiple IDs by space
* `ADMINS`: Username or ID of Admin. Separate multiple Admins by space
* `DATABASE_URI`: [mongoDB](https://www.mongodb.com) URI. Get this value from [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/dsuTn4qV2GA)
* `DATABASE_NAME`: Name of the database in [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/dsuTn4qV2GA)

### Optional Variables
* `OMDB_API_KEY`: OMBD_API_KEY to generate imdb poster for filter results.Get it from [omdbapi.com](http://www.omdbapi.com/apikey.aspx)
* `CUSTOM_FILE_CAPTION` : A custom caption for your files. You can format it with file_name, file_size, file_caption.(supports html formating)
Example: `<b>Join [XTZ Bots](https://t.me/subin_works) for more useful bots</b>\n\n<code>{file_name}</code>\nSize{file_size}\n{file_caption}.`
* `AUTH_GROUPS` : ID of groups which bot should work as autofilter, bot can only work in thease groups. If not given , bot can be used in any group.
* `COLLECTION_NAME`: Name of the collections. Defaults to Telegram_files. If you going to use same database, then use different collection name for each bot
* `CACHE_TIME`: The maximum amount of time in seconds that the result of the inline query may be cached on the server
* `USE_CAPTION_FILTER`: Whether bot should use captions to improve search results. (True/False)
* `AUTH_USERS`: Username or ID of users to give access of inline search. Separate multiple users by space. Leave it empty if you don't want to restrict bot usage.
* `AUTH_CHANNEL`: ID of channel. Without subscribing this channel users cannot use bot.
* `START_MSG`: Welcome message for start command.

## Note
* Currently [API used](http://www.omdbapi.com) here is allowing 1000 requests per day. [You may not get posters if its crossed](https://t.me/ThankTelegram/910168). 
Once a poster is fetched from OMDB , poster is saved to DB to reduce duplicate requests.

## Admin commands
```
channel - Get basic infomation about channels
total - Show total of saved files
delete - Delete file from database
index - Index all files from channel.
logger - Get log file
```

## Tips
* You can use `|` to separate query and file type while searching for specific type of file. For example: `Avengers | video`
* If you don't want to create a channel or group, use your chat ID / username as the channel ID. When you send a file to a bot, it will be saved in the database.



## Thanks to 
* [Pyrogram](https://github.com/pyrogram/pyrogram)
* Original [Repo](https://github.com/Mahesh0253/Media-Search-bot)


## Support
Contact Me On [Telegram](https://t.me/subinps_bot)

[Update Channel](https://t.me/subin_works)

## License
Code released under [The GNU General Public License](LICENSE).
