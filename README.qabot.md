## QABot

This is a Matrix Q&A system built on top of Hebbot. you can use it with vanilla Hebbot from upstream, but the patches in this branch make it smoother

## Concept

- Reporting room == Public room where the talk is happening
- Admin room == backstage room
- Editors == talk moderators

Attendees log questions by tagging the bot, or moderators can add the appropriate reaction emoji. The bot stores this as normal, in store.json. We then use a small vhost and a bit of JS/HTML to expose the JSON store as a custom iframe which can be embedded in the backstage room.

Additionally, an "Answered" section emoji can be configured, which will cause the iframe to strikeout answered questions.

## Caveats

- Hebbot only listens in one room, so this will not work for multi-track conferences (unless you deploy multiple bots)

## Reccomended config

see config.qabot.toml for a sample that uses the patches in this branch

## JS/HTML

See index.html for this - it uses DataTables to render the data

## VHost

TODO

