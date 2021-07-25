# Oxbase.com
A midsize routing node for a few lightning projects. 

- Follow [@oxbased](https://twitter.com/oxbased) for updates. 
- Node Details on [Amboss](https://amboss.space/node/025176c4be908ee06946c27991949391e50af961328469772dd04aead0f951f1cd)
- forwards / month: ~50M sats ($25k)
- Minimum new channel size >5M sats

> [Message me](https://twitter.com/oxbased) to open ballanced channels.



## How I manage it.

I don't have any automation yet. Every week, I do the following.

#### Adjust Fees
- Lower fees 5% on channels with high local balances.
- Raise fees 5% on channels with low local balance and try to rebalance.


#### Balance Channels
Use services to balance their respective channels.

- Move sats to [Coinos.io](http://coinos.io) wallet.
- Withdraw sats from [River.com](https://river.com/signup?r=3ZWPWH7X).
- Send sats to my Wallet of Satoshi

Circular Rebalances: This almost never works for me at reasonable fee levels.


#### Open / Close Channels 
If on chain fees are low <20 sats/vbyte:

- Close channels that I can't re-balance.
- Open channels to services I use.
- Open channels to nodes I think will earn routing fees.



## My Next Node

- Will be only a lightning node and nothing else.
- Still used a pruned bitcoin node to save hosting costs.
- Make 5M sats the minimum channel size. 
- Use Balance of Satoshis to get more details about node interworkings. 
- Write logic to manage channels how I've been doing manually.
- Don't use it as a wallet. Do routing only. Connect my wallet node to the routing node




## Quick Links

#### Network and Chain Explorers

* [amboss.space](https://amboss.space) - lightning network explorer
* [1ml.com](https://1ml.com/) - lightning network explorer
* [Acinq](https://explorer.acinq.co/) - lightning network map
* [mempool.space](https://mempool.space/) - mempool trends and prices
* [bitbo.io](https://bitbo.io/) - quick dense bitcoin stats
* [yalls.org/nodes](https://yalls.org/nodes/) - potentially good routing peers

#### Create Liquidity
* [LightningNetwork+](https://lightningnetwork.plus/swaps/338) - connects node operators to create chains

#### Provision a Lightning Node 
* [Run-LND](https://run-lnd.readthedocs.io/en/latest/) - scripts to setup a lightning node on AWS or linux host
* [BTCPayServer](https://btcpayserver.org/) - open source bitcoin and lightning node with ability to create store
* [lunanode.com](https://www.lunanode.com/) - hosting provider that accepts lightning payments. [Spin up BTCPayserver with just your api keys](https://docs.btcpayserver.org/LunaNodeWebDeployment/).

#### News and Information
* [good twitter follows](https://twitter.com/oxbased/following) - Who I follow on twitter. Also good weekly spaces.
* [investors podcast](https://www.theinvestorspodcast.com/bitcoin-fundamentals/)
* [what bitcoin did](https://www.whatbitcoindid.com/)

#### Random
- Connecting to nodes that have many >100 channels rarely route anything. I suspect this is because many of their channels are not balanced so most attempted transactions fail.
- When using Thunderhub to rebalance, many of the requests timeout because of my nginx settings from BTCPayserver.
- [This](https://github.com/btcpayserver/btcpayserver/discussions/2651#discussioncomment-957878) is how you can edit the lnd settings in BTCPayserver.