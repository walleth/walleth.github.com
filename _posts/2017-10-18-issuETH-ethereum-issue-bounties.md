---
layout: post
image: assets/img/news/issueth_icon.png
title: issuETH - the Github app for issue bounties
---

I really liked the idea of [commiteth](https://commiteth.com/) and wanted to use it for my projects - but had a [problem with the permission model.](https://github.com/status-im/commiteth/issues/56)

![](/assets/img/news/commiteth_permissions.png)

I am not brave enough to give a 3rd party these permissions to my Github account. Unfortunately fixing this is not a simple change to this project that I could just fix via a PR. The fix is to use github-apps and not the old oauth-flow. You can get more details about this problem in a [video of the recent GitHub Satellite 2017](https://www.youtube.com/watch?v=PpFaKCzKsYA)

I figured to get faster to where I wanted to go: it is better to create a project from scratch. So issuETH was born. As it is a github-app - you can easily enable it for your projects. To install it please go to [https://github.com/apps/issuETH](https://github.com/apps/issuETH)

![](/assets/img/news/issueth_install.png)

It requires very little permissions:

![](/assets/img/news/issueth_permissions.png)

Basically you just interact with this bot via issues. If you attach a label with the text "bounty" to any issue on some repository that has issuETH enabled: then issuETH will generate a keypair and comment on the issue with an [ERC-67](https://github.com/ethereum/EIPs/issues/67) QR-Code.

![](/assets/img/news/issueth_erc67.png)

You can then use this QR-Code to add value to this account - e.g. with WALLETH. This does not have to be Ether - this could (and perhaps should) better be tokens. E.g. your project tokens. They don't even need monetary value - you could just us them for voting.
IssuETH is also showing you transactions for this account:

![](/assets/img/news/issueth_tx.png)

The token-definitions are from: [https://github.com/MyEtherWallet/ethereum-lists](https://github.com/MyEtherWallet/ethereum-lists)

Now the crux: how to get the value to the beneficiary. I do not want or cab pay transaction fees for all projects that use this app. Also it is not trivial to always be sure to transfer all possible value from different networks with different tokens.

So what issuETH is doing for now is to hand over the private key to the account that was created by issuETH for this issue to the current assigned user at the point of closing the issue. As I found no way to contact the user with the github API (perhaps this is a good thing :) the solution is to encrypt the private key with the PGP key of the user and answer publicly on the issue.

![](/assets/img/news/issueth_pgp.png)

Sure this is more hands-on than one would like - but I think it is perfectly fine for the MVP. Ideally in the future we can do magic here with smart-contracts and oracles.

I would be happy about feedback. Please try it out (not yet with huge amounts please). If you find issues please let me know.
