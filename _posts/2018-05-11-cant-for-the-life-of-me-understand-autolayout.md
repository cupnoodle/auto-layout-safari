---
layout: post
title: "I can't for the life of me understand Auto Layout"
date: 2018-05-11 18:18 +0800
categories: safari
permalink: cant-for-the-life-of-me-understand-autolayout
---

Source: [https://www.reddit.com/r/iOSProgramming/comments/6tl95r/i_cant_for_the_life_of_me_understand_auto_layout/](https://www.reddit.com/r/iOSProgramming/comments/6tl95r/i_cant_for_the_life_of_me_understand_auto_layout/)

## Pain

- I can't for the life of me understand Auto Layout
- Little did I know that Auto Layout would totally fuck me up
- I'm at the point where I'm to say just **fuck it** and go to another language
- I'm not lying when I say I spent at least 6-7 hours trying to understand StackViews
- Watched a bunch of videos and read Apples Documentation **but it isn't clicking for me**
- When I started putting the constraints for the two StackViews **I kept running into "conflicting constraints" error over and over again**
- How should I go about learning Auto Layout and what not?
- **I really just wanna code** but I feel like I really need to understand Auto layout before I can
- I feel like it isn't normal at all to spend well over 6 hours trying to get a simple UI to work
- Any help would be AMAZING this has been driving me nuts all day.

Commenter's

- In iOS11, I have not been able to find out what the new method of constraining UIViews is, would be nice if Apple included the updated information when they indicate a feature is deprecated (top and bottom layout guides are deprecated)

Solution is safe area - [https://www.bignerdranch.com/blog/wwdc-2017-large-titles-and-safe-area-layout-guides/](https://www.bignerdranch.com/blog/wwdc-2017-large-titles-and-safe-area-layout-guides/)

- Scrollview is the trickier one. Rules are a little bit different for this one

- Don't worry, (Auto Layout) it's very confusing to me as well. Took a lot of time to make sense of it. I still don't like it, but i know how to work with it.

- Apple official docs on Auto Layout don't explain the on key concept you need to understand it, and apple's APIs are so clunky the kind of obscure it.

- Forgotting to set `translatesAutoResizingMasks = false` will totally break autolayout

- Doing auto layout in the interface builder is a pain in the ass.

## Jargon

- Auto Layout
- Swift
- language
- User Interface / UI
- button
- label
- Stack View / StackView
- constraint
- conflicting constraint

## Recommendation

- If you want to understand Autolayout in general go through all the Apple docs slowly and make sure you understand what they mean.
- If I were you I'd avoid stackviews here and just set constraints for each of the 3 items in your UI.
- I'd also recommend not using UIStackView until you fully understand autolayout.
- The main thing to understand is that each UIView must have four constraints: leading, trailing, top and bottom. 
- ^ No, each view needs enough constraints to let it calculate its position and size. This can be done with the 4 you mentioned, but there are dozens of other configurations that are also acceptable.

- You have conflicting constraints, which means there's some place where a view has two constraints that cannot both be in place.
- The error should tell you which UIView is causing problems. If not, you might try deleting your constraints one by one. (Check error message to solve problem)
- If you wanna grasp autolayout stay away from helper libs because they hide some nifty details.
- Read up on intrinsicContentSize if you want custom views integrated with autolayout.
- Stackviews could be overkill +1
- I'd recomend starting with constraining just one view with a simple set of constraints... left, top, width, height.
- What you need to understand is that every constraint is a linear equation like you'd see in high school algebra, Y=mX+b where X and Y are the edges/center/size of some views.
- I prefer [https://github.com/jmfieldman/Mortar](https://github.com/jmfieldman/Mortar) as it's a lot more fully featured(and it has a few niceties like automatically setting translatesAutoResizingMasks which will totally break autolayout if you forget to set it on all your views)

- Learn auto-layout programmatically!
- Constraints are just a really convoluted way of applying CSS-like position and size it got a lot easier to grasp
- You can't really just 'wing it' and get it working with trial and error like you can with most other things
- You need to understand it and set it up methodically.
- Do something simple first.

## Worldview

- It takes a while (to understand Auto Layout) but once it clicks it makes an awful lot of sense.
- As a beginner in iOS, it is normal to spend well over 6 hours trying to get a simple UI to work
- Every developer I know has spent hours before on Auto Layout until it finally "clicked." 
- Practice makes perfect... I used to bang my hand about it... but after you get it it's intuitive
- Stay away from helper libs because they hide some nifty details (Not being able to understand how something work under the hood is not good)
- Autolayout is not that hard and you certainly would not be able to master it in 6-7 hours
- It's more efficient in laying out design in storyboard rather than code (designing UI visually is more efficient than code, no need to imagine how it will look like / build the program to see layout)
- Doing Autolayout / UI in code / programmatically helps learning how it works under the hood
- Took a lot of time to make sense of Auto Layout
- You can't trial and error Auto Layout until it works
- Start simple


