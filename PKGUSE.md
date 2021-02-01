<div align="center">
  <br />
  <p>
    <a href="https://discord.gg/2BQMYyV"><img src="https://cdn.discordapp.com/attachments/702047402328195152/732285388063899668/b75c04ba-ba8f-4057-93c0-9322f33526cf2F20200425_115122.png" width="546" alt="Tnai Logo" /></a>  </p>
  <br />
</div>
{% hint style="success" %}
For any questions enter our discord server: [https://discord.gg/2BQMYyV](https://discord.gg/2BQMYyV)
{% endhint %}

[![downloads](https://img.shields.io/npm/v/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)
[![version](https://img.shields.io/npm/dt/tnai.svg?style=for-the-badge)](https://www.npmjs.com/package/tnai)

An NSFW/Anime Wrapper API that helps how to get random images!


### Installation
{% hint style="info" %}
Using ``npm i tnai``
{% endhint %}

### Getting access token
- Go to **[tnai.ml](https://tnai.ml/)**.
- Open navigation bar (menu).
- Click on **login**.
- Log in with Discord Oauth2.
- Go to the menu and click on **[profile](https://tnai.ml/profile)**.
- Copy the hidden token 

### Fast Example:
```javascript
const tnai = require('tnai'),
cli = new client("YOUR_TOKEN"),
gif = await cli.sfw.hug()

console.log(gif) // Response: https://cdn.tnai.ml/images/aEfk2c8d.gif
```

### Using from command handler:
Basic example:
```javascript
const tnai = require("tnai")
const client = new client("YOUR_TOKEN");
const { MessageEmbed } = require("discord.js");

module.exports = {
"name": "angry",
"usage": "!angry"
run: async (client, message, args) => {
let gif = await client.sfw.angry()
cons embed = new MessageEmbed()
.setTitle("Some title") // Title
.setImage(gif) // Gif from Tnai
.setColor("#ffffff") // Embed color
message.channel.send(embed)
}
}
```

{% hint style="info" %}
Remember to have the latest version.
{% endhint %}
