This is a Telegram Bot that renders the LaTeX syntax in the chat.
The engine of LaTeX is the service provided by https://math.now.sh, so no local LaTeX installation is required.

The workflow is very easy:
- a regexp search in any message for a text between dollars ($something$);
- the https://math.now.sh is called and an SVG image is returned;
- the image has only the Alpha channel different from zero, but I need a true RGBA image, so I use the information in Alpha channel to create the three colors. The idea is to have white background with middle grey text (127 as value), in this way I can render the image with transparent background on both white and dark Telegram setup;
- the image is then converted into WEBP format. This is due to the fact that PNG images are not visualized with transparent background in telegram, so I use WEBP and I send them as stickers, not as images.

To make it working on your computer you need to register the telegram bot in the BotFather and use the token that it will generate.
To be able to use in groups, you need to disable the default privacy setting in the BotFather. So once the bot is created the procedure is to call /setprivacy, select your bot and then click Disable. In this way the bot can receive messages when is in a group, otherwise it will ignore.

The bot as a feature to remove the latex source after the rendering in order to keep clean the chat. This feature works only if the bot is group administrator with the "Delete messages" function enabled.

If you want to try mine it is sufficient that you add <a href=https://t.me/myLaTeXbot>@mylatexbot</a> to your group chat. Please consider that there is no warranty that I will keep it working continuosly, so if you need it for professional reasons, consider to register your own bot.

<img src=https://github.com/emanuelelaface/LaTeXBot/blob/master/screen-shot.png></img>
