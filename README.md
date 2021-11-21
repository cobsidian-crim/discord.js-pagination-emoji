<div align="center">
  <p>
    <a href="https://nodei.co/npm/discord.js-pagination-emoji
/"><img src="https://nodei.co/npm/discord.js-pagination-emoji.png?downloads=true&stars=true" alt="NPM info" /></a>
  </p>
</div>


# discord.js-pagination-emoji
An updated version of the [discord.js-pagination package created by saanuregh](https://github.com/saanuregh/discord.js-pagination) featuring proper discord.js@13.0.0 support and custom emojis!

**If you want to use unicode emojis, please install [discord.js-pagination-v13](https://www.npmjs.com/package/discord.js-pagination-v13)**

# Installation
* `npm install discord.js-pagination-emoji`

# Usage
__Basic Bot Example__
```js
// Import the discord.js-pagination package
const paginationEmbed = require('discord.js-pagination-emoji');

// Use either MessageEmbed or RichEmbed to make pages
// Keep in mind that Embeds should't have their footers set since the pagination method sets page info there
const { MessageEmbed } = require('discord.js');
const embed1 = new MessageEmbed();

const emojiList = ["emoji1ID","emoji2ID"]

// Create an array of embeds
pages = [
	embed1,
	embed2,
	//....
	embedn
];

// Call the paginationEmbed method, first two arguments are required
// emojiList is the pageturners, you must use your own emojis.
// timeout is the time till the reaction collectors are active, after this you can't change pages (in ms), defaults to 120000
paginationEmbed(msg, pages, emojiList, timeout);
// There you go, now you have paged embeds
```
