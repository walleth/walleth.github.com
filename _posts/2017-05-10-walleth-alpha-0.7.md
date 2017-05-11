---
layout: post
image: assets/img/icon.png
title: WALLΞTH 0.7 Alpha
---

Version 0.7 alpha attacks mainly the initial sync problems. I saw a lot of users had crashes there. Some of the errors I saw where reported upstream to the go-team. Some now even have <a href="https://github.com/golang/go/issues/20259">milestones attached</a>. Unfortunately it happened really often in the initial sync with the chain on some devices. These problems are not solved yet but I could gather some more information about them and found a way to mitigate the problem a bit. The crashes only happen when you have to import a lot of headers like with the initial sync. You will not see it that often once you had a full sync and update regularly. For the initial sync I added a watchdog that restarts the app once this happens. I did not find a way to get geth in a working state again once these crashes happened. Also I added a debug screen where you can see the error log:

<img src="/assets/img/news/screenshot_debug.png"/>
![](/assets/img/news/screenshot_debug2.png)

This should help to reduce the frustration for the initial sync. Just open walleth - enable the light client - put your phone in WIFI and attach the charger. Then wait a while. Your phone might get warm. If you see these crashes - please use the share button in the debug activity to share the reports. Or even better look at the reports and try to check if it is one of these issues:

* [https://github.com/ethereum/go-ethereum/issues/14422](https://github.com/ethereum/go-ethereum/issues/14422)
* [https://github.com/ethereum/go-ethereum/issues/14367](https://github.com/ethereum/go-ethereum/issues/14367)

If so please +1 these issues and perhaps add observations that might help getting to the bottom of this. If not please open a new issue or forward the report to me so I can have a look.
I hope we can overcome these problems soon - but thats why I said light-clients/mobile nodes are in a alpha stage..
But as these crashes happened so often I decided to make starting the light client optional for now. So you are not greeted with the high potential of crashes - but you can opt into them if you also find light-clients important and are willing to help make it stable.

![](/assets/img/news/screenshot_with_settings.png)

Unfortunately i did not find a way to make transactions without a node as I cannot yet get the raw bytes to relay them to etherscan for the time being. I opened an issue that could change this: +1s here could also help: [https://github.com/ethereum/go-ethereum/issues/14443](https://github.com/ethereum/go-ethereum/issues/14443)
I also fixed that outgoing transactions now show the "to" field instead of "from" and added an activity to create an account where you could paste a hex.

![](/assets/img/news/screenshot_list.png)

Let me know what you think - constructive Feedback is always welcome!
