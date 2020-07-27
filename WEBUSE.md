# Tnai API

{% hint style="warning" %}
The website "https://api.tnai.ml" is still under development, for now it cannot be used, more news on the support server.
{% endhint %}

[![downloads](https://img.shields.io/npm/v/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)
[![version](https://img.shields.io/npm/dt/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)


A simple endpoint that you can use for Discord.js or other apps, follow reading so you can discover how to use our endpoints.

Some dependencies that you can use: [Snekfetch](https://www.npmjs.com/package/snekfetch) | [Node-fetch](https://www.npmjs.com/package/node-fetch)

### Using with Snekfetch:
Here you will get the SFW category URL:

```js
const request = require('snekfetch');
    request.get('http://api.tnai.ml/sfw/kiss').then(response => { 
    console.log(response.body.url)
});```

### Sending from a MessageAttachment
This method is not compatible with Discord.js v11 version.

```js
const { MessageEmbed, MessageAttachment } = require('discord.js');
    const request = require('snekfetch');
    request.get('http://tnai.ml/sfw/greeting').then(response => {
    const attachment = new MessageAttachment(response.body.url);
    message.channel.send([attachment]);
    });```
