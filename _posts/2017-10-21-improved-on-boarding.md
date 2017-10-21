---
layout: post
image: assets/img/icon.png
title: 0.21 Improved on-boarding
---

Turns out not everyone found the button to transfer value to the account - so I added a ShowCaseView the first time the app starts:

![](/assets/img/news/improved_onboarding.png)

Also now you can delete/undelete tokens and addresses. Especially the token-list this was important as there are so many..

To delete just swipe the token or the address.

![](/assets/img/news/tokenlist_delete.png)

Also [planning on adding a search](https://github.com/walleth/walleth/issues/69) here.

Now you can also set the geth-verbosity so we can track down some connection-problems.
Besides this there where some small fixes. E.g. this one:

[#66 org.json.JSONException: Value <!doctype of type java.lang.String cannot be converted to JSONObject ](https://github.com/walleth/walleth/issues/66)

Or a problem that token-transfers where not correctly displayed in the list.
Also we now use the just released [1.0.0-RC Release-Candidate](https://developer.android.com/topic/libraries/architecture/release-notes.html) of the architecture components.
All in all I see not much blockers for moving from alpha to beta - I only see [#58](https://github.com/walleth/walleth/issues/58) and [#56](https://github.com/walleth/walleth/issues/56) currently.
Please if you find bugs: report them!

Also there is now a [matrix-room for WALLETH](https://riot.im/app/#/room/#walleth:matrix.org) for questions and suggestions around WALLETH.
