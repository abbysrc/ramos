<div align="center">
  <img src="https://i.imgur.com/vfliY0x.png" width="100"></img>
</div> 
<h2 align="center">Ramos: an open-source bot for creating shopping packages in your Discord community</h2>   
<b align="center">Still in dev phase, more code coming soon!</b>
  
<hr />
  
## About Ramos
Ramos is developed & maintained by hanatic, plus the help of anyone else who turns up (see image below. Just the concept of it has gone through many revisions: it first began as a project called Hyview, working with the Hypixel API to create a platfrom like [HyAuctions](https://auctions.craftlink.xyz), which was later abandoned (because I just cannot work out how to use hooks in React - it's my one flaw). This then evolved into a theorised platform to make purchasable packages on Hypixel Skyblock that could be purchased through Discord. Financial troubles intervened and I decided to open source the code. Not quite finished yet though, a few features need polishing and I definitely plan to expand it.

## Contributors  
<a href="https://github.com/hanatic/ramos/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=hanatic/ramos" />
</a>

## Prerequisites
- A Discord account
- A Discord bot token (can be obtained via https://discord.com/developers/applications), with the bot added to a server you are on
- Git installed locally
- NPM installed locally
- TSC && TS-node installed locally (`npm i tsc ts-node -g`)
- MongoDB client installed locally
- Either a local MongoDB server or an instance in the cloud (https://atlas.mongodb.com)

## Installing

1: Clone the git repository, enter it in your terminal and install the dependencies
```
git clone https://github.com/hanatic/ramos
cd ramos
npm install
```

2: Add your token to line 10 of src/index.ts

```js
// ...
import packages from './package';

/* put it here >>> */ var token = "YOUR_TOKEN_HERE";
// ...
```

3: Add your Mongo URL in line 16 of src/index.ts

```js
// ...
mongoose.connect("<YOUR URL WILL GO HERE>", {
    useNewUrlParser: true,
    useUnifiedTopology: true,
    useCreateIndex: true               // to handle collection.ensureIndex is deprecated
})
// ...
```

4: (optional) Install `ts-node-dev` - this helps you reload the TypeScript code - useful if you plan to edit it.
```
npm i -g ts-node-dev
```

5: Run the app: if you installed ts-node-dev:
  ```
  npm run dev
  ```
If you didn't:
  ```
  ts-node src/index.ts
  ```
  
6: Make sure it's working: you should get console output like this (tag will be different)
```
Ramos#6914 has logged in using Ramos.
```

( 7: You're going to want to add your packages in src/package.ts - if you know a little about TypeScript it should be relatively easy to understand )

## Support
Join our discord: https://discord.gg/ySbSesFNB5

## alright thats us done, peace out
