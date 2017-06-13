---
layout: post
image: assets/img/icon.png
title: Offline transactions
---

WALLETH 0.14 is about "offline transactions". This is a security feature - a bit like a hardware wallet.
The Idea is that you have WALLETH on 2 separate phones:

 * One phone (e.g. your daily driver) has Internet access and some account in watch-only mode
 * Another phone (e.g. an old phone where you perhaps even removed the GSM and WIFI antennas) has no Internet access and holds the key for the account

 ![](/assets/img/news/offline_transactions.png)

 You prepare the transaction on the first phone. In the transaction-details you see then a QR-Code with the unsigned RLP. With the other phone you scan this code & sign the transaction. This phone then shows you an QR-Code with the "signed RLP".
 Yes this is a bit of ugly QR-Code juggling - but it also has nice properties:

  * cheap - you might have this old phone in your drawer but would need to buy a hardware wallet
  * you can visually inspect the very restricted communication. You can e.g. see if a QR-Code contains a lot of data or not (by the size of the dots) - also you are clearly aware of the direction of communications. With hardware wallets you cannot see easily which data is exchanged on the wire between the hardware-wallet and the internet-connected and untrusted device.

You can later even combine this feature with hardware wallets for very sensitive accounts/use-cases. I am currently preparing [TREZOR](https://shop.trezor.io) support in WALLETH. If you want to have a peek behind the curtains: [relevant PullRequests](https://github.com/trezor/trezor-android/pulls?q=is%3Apr+is%3Aclosed) & [relevant issues](https://github.com/trezor/trezor-android/issues?q=is%3Aissue+is%3Aclosed)

Currently only WALLETH<>WALLETH is supported. But as soon as [this issue](https://github.com/ethereum/go-ethereum/issues/14599) with the geth mobile API is solved the offline part can also be done with [MyEtherWallet](https://www.myetherwallet.com).
