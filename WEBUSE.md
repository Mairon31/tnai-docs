# Tnai API

{% hint style="sucess" %}
The "https://tnai.ml" website can now be used!.
{% endhint %}

[![downloads](https://img.shields.io/npm/v/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)
[![version](https://img.shields.io/npm/dt/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)


A simple endpoint that you can use for Discord.js or other apps, follow reading so you can discover how to use our endpoints.

Some dependencies that you can use: [Snekfetch](https://www.npmjs.com/package/snekfetch) | [Node-fetch](https://www.npmjs.com/package/node-fetch)

### Using with Snekfetch:
Here you will get the SFW category URL:

```js
const request = require('snekfetch');
    request.get('https://tnai.ml/api/image?type=hug', {
    headers: {
    "Authorization": "YOUR_TOKEN"
    }
    }).then(response => { 
    console.log(response.body.url)
});```

### Sending from a MessageAttachment
This method is not compatible with Discord.js v11 version.

```js
const { MessageEmbed, MessageAttachment } = require('discord.js');
    const request = require('snekfetch');
    request.get('https://tnai.ml/api/image?type=hug', {
    headers: {
    "Authorization": "YOUR_TOKEN"
    }
    }).then(response => {
    const attachment = response.body.url;
     message.channel.send([attachment]);
    });
```
