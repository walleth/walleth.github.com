---
layout: post
image: assets/img/icon.png
title: Thoughts on the UX of payment channels
---

While traveling through hostels the last month I realized payment channels - even the simple 1:1 form that is coming with the [soon to be released µRaiden](https://github.com/raiden-network/microraiden/milestone/2) - would be a great fit here. You often have to pay for things while you stay. For renting your bike, for making your laundry or for extending your stay.
So I thought a bit how this could be nicely integrated with WALLETH user flows. My idea is that you can jump into the flow by checking a special option in the create transaction activity/flow. You just check "Enable payment channel" and then you get one extra option to select the deposit for it. I am not yet sure about the naming here - is payment channel really the term that should surface to the end-user or better something like "recurring payments"?
Then when you do another transaction and it is detected that you have an open payment channel with this peer you get the option to use it. Perhaps also do it by default - I am not yet sure if there are use-cases where you would not want to use the open channel - but do it as a normal transaction. If you know use-cases like that I would be most interesting in knowing!
I think doing it like this and not building a special user flow for the payment channels has several benefits:

 * The user will be exposed to this option often - so the discoverability is high and at the right time (sees it when it can be used)
 * The user does not have to learn many new concepts
 * Lot of (mainly UI) code can be reused

What I was also thinking about was that maybe often you want to combine opening of a channel with an initial payment - e.g. in the hostel for the first night. Not sure if this would save significant fees - but UX wise it is beneficial as you can have faster flows. Instead of a 2 step process (#1 open channel, #2 use channel to pay) to a one step process (open and do initial payment)

Sure this is not limited to hostels - I just ideally need a real world use-case to think about user flows. I could also see this being used in your favorite club, restaurant, cinema, bar, transport-provider, tool-renal, milk-station, water-station, streaming-provider, pharmacy, gelateria, power-provider, ..
