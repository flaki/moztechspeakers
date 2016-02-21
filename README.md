# Mozilla TechSpeakers support app experiments

Experiments for supporting Mozilla TechSpeakers via various apps, web services etc.

## _TinSpeaker_ experiment

TinSpeaker is an experiment researching the features of the [Telegram API].

Sources are located in the `/tinspeaker` directory. The code lets you send
messages to the Telegram API, by creating a [Telegram bot] (we are using the
[mozTechSpeakersBot]).

You need to provide `config.json` in the root with your credentials:

```
{
  "TELEGRAM": {
    "BOT_ID": "bot0000000",
    "ACCESS_TOKEN": "...",
    "CHAT_ID": "000",
    "CHAT_ID_DEBUG": "000"
  }
}
```

`BOT_ID` is the ID of the created bot, `ACCESS_TOKEN` is the Telegram-provided
access token, `CHAT_ID` & `CHAT_ID_DEBUG` are the id-s for the chatrooms you
want your bot to interact with.

Launch the app locally via node.js by running:

```
$ node tinspeaker/server.js
Tinspeaker server started on http://localhost:8000/

```
After the server is started and open `http://localhost:8000`. You can use the
debug Chat ID by providing `#DEBUG` in the url. You should provide your own
chat ID with the bot in the `CHAT_ID_DEBUG` variable for testing.

You can now use the textbox to send messages (also, you can use
[simplified markdown] formatting in your messages).

[Telegram API]: https://core.telegram.org/api
[Telegram bot]: https://core.telegram.org/bots/api
[mozTechSpeakersBot]: http://telegram.me/mozTechSpeakersBot
[simplified markdown]: https://core.telegram.org/bots/api#formatting-options
