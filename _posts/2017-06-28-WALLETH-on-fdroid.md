---
layout: post
image: assets/img/icon.png
title:  WALLΞTH available on FDroid
---

The flavor for FDroid was available since the beginning. I love the concept of a store that only contains libre apps and 14 other apps of mine are already available there (e.g. have a look at [PassAndroid](https://github.com/ligi/PassAndroid) or the [Offline SurvivalManual](https://github.com/ligi/SurvivalManual)) But the release to FDroid took a while for WALLETH. The reason was that WALLETH already depends on the google maven repository which was just accepted by FDroid recently (with [MR #275](https://gitlab.com/fdroid/fdroidserver/merge_requests/275)). I want to use the new architecture components like Room, LiveData and the ViewModel - and they only exist in this new repository.

[![on FDroid](http://ligi.de/img/fdroid_badge.png)](https://f-droid.org/repository/browse/?fdid=org.walleth)

Be aware that this flavor does not contain any closed source code. This also means that firebase is not baked in and hence you do not get push messages. On Google-IO 2017 [google announced](https://opensource.googleblog.com/2017/05/open-sourcing-firebase-sdks.html) that the client libraries for firebase will become open source - but until then we cannot use them on firebase.
