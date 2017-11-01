---
layout: post
image: assets/img/icon.png
title: WALLETH at DevCon3
---

I am just writing this sitting in my last connection flight (3/3) to Cancún in Mexico to attend DevCon3. I will give a [short talk](https://ethereumfoundation.org/devcon3/sessions/introduction-to-walleth-the-ethereum-android-wallet) in the morning of day #2 and a longer [deep dive session](https://ethereumfoundation.org/devcon3/sessions/deep-dive-into-walleth-the-ethereum-android-wallet/) in the evening of the same day. I am very much looking forward meeting some interesting people that I only communicated online so far, reconnect with people that I already know and meet some new ones. Looking forward to some great conversations!


![](/assets/img/news/cancun_flight.jpg)

I also hope we can get a [working-group to formalize URLs/QR-codes](https://github.com/ethereum/EIPs/pull/681#issuecomment-340258656) for ethereum together. Currently this is a bit of a wild-west and we need some formalized standard to improve interoperability. DevCon3 is a great place to get this going as a lot of Ethereum-Wallet developers will be there.

For DevCon3 I am releasing WALLETH 0.23 which does not come with new features, but some fixes and polising. Was just making some finishing touches in the hostel.

![](/assets/img/news/cancun_hostel.jpg)

 One of these fixes came via a [PR of Dr. Christian Reitweiser](https://github.com/walleth/walleth/pull/73) from the Ethereum Foundation. When using the main-net: the etherscan URLs where not assembled correctly. They looked like this: https://.etherscan.io/api/.. instead of https://etherscan.io/api. This was no problem with Browsers like Brave - but resulted in non working links for FireFox. Thanks a lot for this PR!
The new Version also contains a Fix for a crashbug that happened on some devices caused when [using ellipsize and lines="1"](https://issuetracker.google.com/issues/36950033) in combination - which I did for some hashes. Also the QR-Codes now got way sharper and better looking as I disabled antialiasing for them. Speaking of QR-Codes - also the offline Transaction Flow was fixed - unfortunately this was broken since the network-switching was introduced.
WALLETH 0.22 also contains some things that end-users will not see like updated libraries and improvements for the UI-tests.

Hope to see some of you at DevCon3!
