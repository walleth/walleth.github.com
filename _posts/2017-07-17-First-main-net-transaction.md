---
layout: post
image: assets/img/icon.png
title: First transaction on main-net
---

And so this begins - WALLETH slowly grows out of alpha and gets ready for the Ethereum main-net. I do not want to waste real value for testing so everything was on rinkeby before.

Here you find [the first main-net transaction](https://etherscan.io/tx/0x2ee22edf810db058058a2de0d82623ac8347873d643c761fca8fa2c38ee2aa45).

![](/assets/img/news/screenshot_network_switch.png)

If you have a better idea for the icon than the flag: please let me know - ideally in the form of a vector-image ;-)

Would also like to try out ERC-20 tokens on the main net - so if you have some: I am happy about samples - fractions of them are enough to test!

<strike>I could also use some ropsten test-ether to try out the switch to this network. Unforunately the faucet  found for ropsten is dry :-(</strike> Got some on /r/ethdev and successfully transfered some around.

In other WALLETH news: I recently implemented EIP55 checksums in [ketherum](https://github.com/walleth/kethereum). And implemented the usage of it for creating addresses in WALLETH (via generating a key or reading from <a href="https://TREZOR.io">TREZOR</a>). For implementing EIP55 I needed a keccak implementation and so there is now a [pure kotlin implementation now](https://github.com/walleth/keccak).

But I still love rinkeby - and remember- it is [not a "no go zone"](https://www.somalispot.com/threads/rinkeby-is-not-a-no-go-zone-song.23723/) ;-)
