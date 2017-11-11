---
layout: post
image: assets/img/icon.png
title: A case for lighter light clients
---

Google-Play has this new thing called "Android Vitals"  - that means there are some indicators that can flag your app as behaving badly and so get penalized in Google-Play search.

![](/assets/img/news/vitals_shot.png)

Unfortunately current light-client implementations are still very heavy in consuming data and CPU cycles.


![](/assets/img/news/screenshot_light_data_usage.png)

This sadly now also means apps that do the right thing and enable/encourage light-client usage get penalized by Google-Play :-(

But there is hope on the horizon - [zsfelfoldi is working on lighter clients](https://github.com/ethereum/go-ethereum/pull/14970) And spoke to him at DevCon3 - things might look bright in the future as he has some ideas on how to attack the problems. But I think more people should work on this problem. I think light-clients are a critical part of the road that leads to Ethereum mass-adoption.

![](/assets/img/news/light_client_is_experimental.png)
