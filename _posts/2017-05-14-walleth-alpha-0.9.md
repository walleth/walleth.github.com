---
layout: post
image: assets/img/icon.png
---

Making running the node optional highly reduced the crash-rate - but also crippled the functionality as sending transactions needed the node to be running. I had an idea in mind how to metigate this, but the API from the in-process node [did not yet offer the required functionality](https://github.com/ethereum/go-ethereum/issues/14443). But the go-team just needed 3 days from request [to implementation](https://github.com/ethereum/go-ethereum/pull/14454) - so great - big shout out to Péter Szilágyi aka karalabe!
![](/assets/img/news/screenshot_new_transfer.png)

In this process I exposed the fee-values and linked to [ethgasstation](http://ethgasstation.info) so users can adjust the values in an informed way. At some point I will hide this behind some advanced setting but for now this should be OK as most users (currently) have a ethereum/tech background anyway.
