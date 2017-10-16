---
layout: post
image: assets/img/icon.png
title: Byzantium & Network switching
---

It was a bit quiet here the last 2 months - but unfortunately I had to work on one commercial project to pay some bills. But now I have time again to push WALLETH forward - and I was just pushing it over 2 bumps:

 * Network switching (inclusive main-net:-)
 * Byzantium changes (Contains geth 1.7.1)

Please note even though this version only includes geth 1.7.1 there should be no problem. The most recent 1.7.2 is only important for full-nodes. I still would love to include 1.7.2 (also as it includes [#15233]( https://github.com/ethereum/go-ethereum/pull/15233))
Unfortunately gomobile was recently updated and builds for the go-ethereum android library started failing on Friday the 13th :-(

There are also a lot of small detail changes in this version. E.g. you can now clearly see watch-only accounts. Also the last used account is now remembered.

![](/assets/img/news/list_with_watchonly.png)

In the transaction list you can now see the state of the transaction.

pending unsigned: ![](/assets/img/news/ic_lock_open_black_48dp.png)
pending signed: ![](/assets/img/news/ic_lock_outline_black_48dp.png)
confirmed: ![](/assets/img/news/ic_lock_black_48dp.png)

There are also a lot of changes under the hood. WALLETH now uses the [architecture components](https://developer.android.com/topic/libraries/architecture/index.html) that Google announced at IO this year. Especially room and LiveData is a nice fit for this application.

Also Kotlins co-routines are used now. They are still in experimental stage. But a talk at DroidCon Berlin this year convinced me to already use them as JetBrains stated it is only declared experimental so they can change the API - but it is already stable.

Please note that although this version now contains main-net support - it is still in alpha. Please use it with small amounts and low-importance accounts for now. And Ideally use it together with a Hardware-Wallet like the the [TREZOR](http://walleth.org/2017/07/14/0.17-TREZOR-AND-MORE/)
