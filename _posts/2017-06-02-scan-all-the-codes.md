---
layout: post
image: assets/img/icon.png
title: Scan all the codes
---


![](/assets/img/news/scann_all_the_codes.jpg)

WALLETH 0.13 improves the scanning
[FAB](https://material.io/guidelines/components/buttons-floating-action-button.html) on the main screen. Before only [ERC-67](https://github.com/ethereum/EIPs/issues/67) was supported - but unfortunately this is not the reality of the current ecosystem. There are way more types of barcodes without context in the form of an URI out there. Now when scanning from the main screen the following types are detected:

 * ECDSA raw private key (e.g. what [myEtherWallet](https://myetherwallet.com/) uses on the paper wallet)
 * JSON style private key (e.g. from WALLETH on another Android device)
 * HEX address (e.g. from [metamask](https://metamask.io) - then you get asked if you want to add to address-book or initiate a transaction)
 * ERC-67 URI (hope this gets used more and more - and it [looks this is the case](https://github.com/MetaMask/metamask-plugin/issues/1479))

![](/assets/img/news/screenshot_list.png)

This closes [#12](https://github.com/walleth/walleth/issues/12) - thanks to David Albrecht for the feedback!
Let me know if you think there is a barcode type missing or you have any other idea/comment/issue!
This version now also updates geth version to 1.6.3(\*) - so syncing speed is improved by the [great work of karalabe](https://github.com/ethereum/go-ethereum/pull/14545).

(\*) unfortunately 1.6.5 is not yet available via maven-central - but most stuff in there is for the main-net anyway so it is not that important right now
