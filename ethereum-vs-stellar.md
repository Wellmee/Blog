# Ethereum vs. Stellar: Choosing the Right Platform for Wellmee Tokens 
At Wellmee we're building a mobile app, that enhances people's wellbeing. The app is a part of an ecosystem of employees, employers and marketplaces where people can exchange value through the use of a cryptocurrency token. 

From the beginning, we knew that we don't want to build our token infrastructure from scratch. Nowadays there are quite a few established platforms where you can launch your token, so creating another one makes no sense.  As we wanted to use a widely adopted platform, our choice narrowed down to Ethereum vs. Stellar. 

When choosing the platform to launch our tokens we evaluated several criteria. Following is a list of our criteria, for each we're describing Wellmee unique and not-so-unique needs and how Ethereum and Stellar fit into the scheme of things. 

## Implementation Complexity 
At the current stage of Wellmee development we have to be thoughtful about time and budget. Therefore we need a  platform where launching a token would be as technically uncomplicated as possible. Wellmee tokens serve for exchanging value between the ecosystem users, so nothing too innovative on this side. All Wellmee innovation is coming in the mobile app, enhancing lives of our users. 

When you want to launch a simple token on Ethereum, you have to write a good deal of [Solidity code](https://github.com/ethereum/solidity) to define all the parameters of your token, plus some things you don't really want to define, like methods for transferring balances from one account to another. While there are many tutorials on how to do that, there are still challenges you have to deal with, like [overflows](https://ethereum.stackexchange.com/questions/7293/is-it-possible-to-overflow-uints). Everything is documented, but it takes time and effort to get your Solidity code right. 

Stellar has an abstraction called [asset](https://www.stellar.org/developers/guides/concepts/assets.html) that fits closely to what we want to do with Wellmee tokens. It has all basic mechanisms built in, so you just define the basic parameters like volume and decimals and you don't have to dig deep into low-level details. While the Stellar asset isn't as customizable as Ethereum tokens, for us simpler is better.

Winner: *Stellar* 

## Security
Security is the most important thing for Wellmee. We are fully aware of the trust our users put into the app and the ecosystem, and we don't want to take any unnecessary risks here.  

With Ethereum, you get a full-blown Turing complete virtual machine in each node of the computing network. That means you can do pretty much anything, but it also means a lot of things can go wrong. For Ethereum tokens, there's [the ERC20 Standard](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) that almost all new tokens adhere to. The issue is that it only tells you what methods you should define, not how to implement them. So you can easily have a ERC20 compliant token, that is not secure at all. Solidity language design has [quite a few specifics](https://news.ycombinator.com/item?id=14691212) that make it difficult to get the smart contracts right. Moreover there's a lot of potential for bugs on the platform side. There are [Solidity compiler bugs](https://solidity.readthedocs.io/en/v0.4.24/bugs.html) and the complex [Ethereum Virtual Machine](https://gavwood.com/paper.pdf). There's a great community around the platform, but still quite a few things that can go wrong. The security unease was best shown in the infamous [DAO hack](https://en.wikipedia.org/wiki/The_DAO_(organization)). Some experts claim the issue wasn't just with the DAO Solidity code, but [Ethereum itself](https://nakamotoinstitute.org/mempool/ethereum-is-doomed/). We're not saying that Ethereum isn't secure by itself, but launching your own token that is secure takes time and expertise. 

Stellar only provides a fixed set of [operations](https://www.stellar.org/developers/guides/concepts/operations.html) that developers can use to work with tokens. For us it means there's less things to implement and less things that can go wrong. [Attacks on Stellar](https://www.coindesk.com/400k-hacker-makes-off-with-stellar-lumens-in-blackwallet-theft/) have only been made on some of the third party wallets, not the platform itself. As with any other cryptocurrency, our users need to make sure they're using a trusted wallet and keep their secret keys secure. 

Winner: *Stellar* 

## Adoption
With our initial offering, we want to reach as many backers as possible. If the backer already has some funds on the network, they are more likely to buy Wellmee tokens. 

At the time of writing, Ethereum market cap is roughly seven times higher than Stellar ([$28B](https://coinmarketcap.com/currencies/ethereum/) vs. [$4B](https://coinmarketcap.com/currencies/stellar/)). While Ethereum is much bigger, Stellar isn't really small either, and has [some successful ICOs](https://www.coindesk.com/why-a-39-million-ico-chose-stellar-over-ethereum/) in its portfolio. 

Winner: *Ethereum* 

## Access to Tokens
Wellmee tokens should be easy to buy and sell, so that the app users and partners can freely trade the tokens for whatever currency they like. 

Ethereum-based tokens need to be listed on a [cryptocurrency exchange](https://en.wikipedia.org/wiki/Cryptocurrency_exchange) to allow users trade tokens freely. Exchange listing involves a lot of effort to fulfill the requirements of different exchanges. There's usually significant cost and regulatory issues on some markets. 

Stellar comes with a [decentralized exchange](https://www.stellar.org/developers/guides/concepts/exchange.html) built in. That means users can put an offer for any token in the network and trade it for Lumens, or any other asset available. With the [first USD anchor launch](https://medium.com/strongholdxchg/stronghold-stellars-first-venture-backed-usd-anchor-30cf88fc3eb4) this is becoming a strong feature of the Stellar platform. 

Winner: *Stellar* 

## Transaction Speed and Cost
Wellmee tokens are intended to be used in our partner network for real-world goods and services. It's important to have the transactions fast enough, so that our users don't have to wait hours to see a transaction go through. The tokens could be used for small payments, so we don't want to end up in a situation where the transaction fee is higher than the payment itself. 

The Ethereum network works on the [proof-of-work](https://en.wikipedia.org/wiki/Proof-of-work_system) principle. In a simple language, there's a bunch of miners that [work on cryptographic challenges](https://github.com/ethereum/wiki/wiki/Mining) to confirm your transaction. The transactions can be chosen by the miners, so the more you pay for your transaction, the faster it will [go through](https://ethgasstation.info/). At peak times, transactions can become slow or expensive. For us, when using the token in the partner network, this can be an issue. There are plans to transition to a proof-of-stake algorithm, that could improve things. 

Stellar confirms transactions through the [Stellar Consensus Protocol](https://medium.com/a-stellar-journey/on-worldwide-consensus-359e9eb3e949). Using distributed consensus algorithm, the nodes in the network agree on the right set of transactions to confirm. Since there's no hard cryptographic work to be done in mining, the transactions go through fast. Compared to Ethereum, the transaction volumes are much lower, but [stress testing](http://gostellar.io/heir-io-stress-test-over-stellar-beats-their-expectations/) is showing that the network should scale very well. This means fast and cheap transactions. 

Winner: *Stellar* 


## Conclusion
After a careful consideration, we're going with Stellar as the platform of choice for Wellmee tokens. We're excited to see Stellar platform grow and hope we can be a flourishing part of the Stellar world. 