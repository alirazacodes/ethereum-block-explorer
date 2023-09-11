# Ethereum Block Explorer 🚀

I've been diving deep into the Ethereum JSON-RPC API and `ethers.js` this week. With all the knowledge I've gained, I've embarked on an exciting journey to create my very own **Ethereum Block Explorer**! 🌐

What's a Block Explorer, you ask? Well, it's a magical tool that lets you peek into:
  * The vast Ethereum network 🌍
  * Details about individual blocks 📦
  * Transactions within those blocks 🔄
  * Specific Ethereum accounts 📒
  * And so much more!

If you're curious, [Etherscan](https://etherscan.io/) is a prime example. But hey, why not create one myself? 🛠️

## Let's Begin! 🚀

First things first, I've set up some starter code for you. Clone my project and see what's inside.

Now, navigate into the main project directory and fire up `npm install` to get all those juicy dependencies.

I decided to give React a spin for the front-end, but the world's your oyster—choose your weapon! I've sprinkled in some AlchemySDK goodness for that extra flair. 💫

And hey, if you're wondering about the differences between `ethers.js` and AlchemySDK, they're almost the same! 

For instance:
```js
const blockNumber = await provider.getBlockNumber();
```
Translates to:
```js
const blockNumber = await alchemy.core.getBlockNumber()
```
Simple, right? 

And if you ever need the full firepower of `ethers.js`, just grab the provider like:
```js
const ethersProvider = await alchemy.config.getProvider();
```

Dive into the [AlchemySDK docs](https://docs.alchemy.com/reference/alchemy-sdk-quickstart?a=eth-bootcamp) if you're curious. They've been my guide!

## Set Up the Stage 🎬

1. **Alchemy API Key**: First, get your hands on a unique Alchemy API Mainnet key [here](https://docs.alchemy.com/reference/api-overview?a=eth-bootcamp).
2. **Environment Magic**: Create a `.env` file in the project root. Fill it with your key like this:
```sh
REACT_APP_ALCHEMY_API_KEY=YOUR_ALCHEMY_API_KEY
```
Remember to keep that `REACT_APP_` prefix; it's React's magic wand! 🪄

⚠️ A quick heads-up: 
> Always guard your Alchemy API Mainnet Key. It's sensitive! Though for this project, we're good. We're here to learn and have fun, not to conquer (yet)! 😉

3. **Summon the Web Server**: Just type `npm start` and watch the magic unfold at [http://localhost:3000](http://localhost:3000). Instant feedback as you code!

Now, while the starter code gets you the current block number, that's just the beginning. There's a world of possibilities ahead!

## Time to Shine! 🌟

1. **Block Info**: Can you fetch more details about the current block? Hint: [alchemy.core.getBlock()](https://docs.alchemy.com/reference/sdk-getblock?a=eth-bootcamp) might be your friend.
2. **Transaction Tales**: How about extracting the transaction list of a block? Or diving deep into individual transactions? There are methods like [alchemy.core.getBlockWithTransactions()](https://docs.alchemy.com/reference/sdk-getblockwithtransactions?a=eth-bootcamp) and [alchemy.core.getTransactionReceipt()](https://docs.alchemy.com/reference/sdk-gettransactionreceipt?a=eth-bootcamp) to assist you.

## Unleash More Ideas! 🌊

- **Interactivity**: Let users click on a block to see its details, or even click on a transaction to see its nitty-gritty.
- **Account Page**: Fancy a page where users can check balances? Both theirs and others? 😉

## Power Up with AlchemySDK! 🔥

With AlchemySDK, there's a treasure trove of features waiting to be explored:
  * Nifty NFT methods 🖼️
  * Real-time WebSocket methods 📡
  * Unique Alchemy Transact API functionalities 🔄
  * Handy webhook endpoints 🎣

Wondering what you can create? How about fetching an NFT's metadata using its contract address and token id? Or maybe figuring out the current floor price of an NFT? The sky's the limit!