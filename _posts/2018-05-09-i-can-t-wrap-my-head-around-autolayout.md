---
layout: post
title: I can't wrap my head around AutoLayout
date: 2018-05-09 04:20 +0800
categories: safari
permalink: cant-wrap-head-around-autolayout
---

Source: [https://www.reddit.com/r/iOSProgramming/comments/7hc5xl/i_cant_wrap_my_head_around_autolayout/](https://www.reddit.com/r/iOSProgramming/comments/7hc5xl/i_cant_wrap_my_head_around_autolayout/)

## Pain

- Until now, I always avoided the constraints and Auto Layout
- When I first tried it, I already saw that this was probably going to kill me
- And now, where the code part is done and the UI needs to get fixed for all devices, I'm here with my suspicion confirmed. 
- **I might kill myself soon** with **5 months of coding work basically thrown away**.
- For real though - how would anyone go about doing constraints for layouts like those?
- I mean, on some UIViewControllers with a button and a label like in those tutorials, no problem at all. But for setups like those? [http://prntscr.com/himh0d](http://prntscr.com/himh0d)
- Whatever I try, it's either conflicting or
- When I finally got it all blue and think "That's it!", but then go to see it on another device, it all looks absolutely horrible
- I think I've watched and read about 30 tutorials on AutoLayout up to now.
- It would be MUCH easier if I just designed the UI for every single iPhone and iPad by it self
- Can anyone direct me anywhere, how I would go about wrapping my head around this bullshit?

## Jargon

- AutoLayout / Auto Layout
- Swift / Swift Language
- Constraint
- UI / User Interface
- Layout
- UIViewController
- Button / UIButton
- Label / UILabel
- Conflicting (Constraint)
- iPhone
- iPad

## Recommends / Buys
- I used to use the visual format for writing AutoLayout constraints, but found that it was a real source of my problems – no auto-complete, and very cumbersome to update any time you need to add in a new element. This all lead it to being very error-prone, so I'd recommend steering clear from that.
- My favourite methods are now instead either using UIStackViews (completely removes the need to set any constraints) or the anchors APIs (might be relatively new; iOS 9 or something, maybe..?)
- I would also note that the UIStackView method of UI layout is rather similar to CSS3 Flex(ible) Box. Would be more than happy to do all my layout in HTML if it could be done natively, to be honest.
- The problem with auto layout is that winging it as you go along is not an option. With coding you often can, so we are used to it. You need a firm grasp of what is going on before doing anything, and trying stuff until you get it right isn't really much of an option.
- Also never accept Apple's suggestions, they are, well, bad :)
- I recommend trying to learn the concepts. Go view all the WWDC tutorials etc. I kinda gave up on tutorials as they mostly were concerned about building a UI, instead of explaining the concepts and trying to teach correct ways of doing thing.
- Autolayout isn't magic and isn't unwieldy to use. It just have a higher than usual threshold to be useful
- Auto-layout needs to be properly understood and applied systematically. So make sure you understand what every single constraint is doing, throwing them in at random until its 'all blue' is never going to work.
- Also fewer and more generic constraints == better
- using a 3rd party layout library (like LayoutKit) or doing it by hand.
- We sometimes do it by hand. In every viewController, we have a method that repositions the views however we want. It's a little tedious, but extremely fast and flexible.
- The key to autolayout, beyond the technical tidbits, is understanding that you are creating a bunch of rules and the rules have to be consistent and have to fully describe valid positions and sizes of every view. 
- Watch the WWDC videos to get a better understanding of it.
- I found this talk really helpful for having a deeper understanding of how Auto Layout works. [https://www.youtube.com/watch?v=xjArhdrqAn8&t=1073s](https://www.youtube.com/watch?v=xjArhdrqAn8&t=1073s)
- Use stack views to simplify some of the constraint logic.
- I recommend searching on stackoverflow when u have some complex layout, there is always a question about that, but remember to always reads and understand the answer, try to dont copy and go.
- Don't try to add autolayout to an already complex layout, do it step by step in a new project. That should help with getting a grasp on how it works.
- Try Snapkit
- Try Carthography
- Watch WWDC videos, read and experiment. Go to meetups (join mine if you’re in LA) and connect with the community.

## Worldview

OP's

- I really want to ship my own app
- Confident on using Swift language
- Self motivated to learn stuff (watched and read about 30 tutorials on AutoLayout)
- Want the app UI to look good on all devices <- care about good user interface design
- Able to follow tutorial to make the UI as explained in the tutorial, but no idea how to do when making own UI / layout
- Prefer to design fixed UI for each of the screen size
- Anxious / afraid of Auto Layout
- Auto Layout doesn't make sense to me

Commenter's

- There are many alternative ways of specifying the constraints in case you don't get on with one method (Auto Layout constraint via Interface builder GUI), **"dont need to stick to the interface builder Apple gave you"**, **"use whats best for you"**
- Steer clear from visual format for writing AutoLayout constraints, it was a real source of my problems – no auto-complete, and very **cumbersome to update any time you need to add in a new element**. **"Need to make change to many elements contraint if a new element is added, this causes repeatition"**
- The problem with auto layout is that **winging it as you go along is not an option**. With coding you often can, so we are used to it. **"cant trial and error your way out to get the correct result in auto layout"**
- You need a firm grasp of what is going on before doing anything, and trying stuff until you get it right isn't really much of an option.
- Also never accept Apple's suggestions, they are, well, bad:)
- Autolayout isn't magic and isn't unwieldy (difficult) to use. It just have a higher than usual threshold to be useful. **"Auto Layout is not that hard, just that it might not worth the effort"** 
- Auto-layout **needs to be properly understood and applied systematically**. So make sure you understand what every single constraint is doing, **throwing them in at random until its 'all blue' is never going to work.**
- You can ship great iOS apps without autolayout, but it means using a 3rd party layout library (like LayoutKit) or doing it by hand. **"You have to manually code to cater for different screen size or use 3rd party library"**
- The key to autolayout, beyond the technical tidbits, is **understanding that you are creating a bunch of rules and the rules have to be consistent and have to fully describe valid positions and sizes of every view**.
- **Its just trying**. Its really hard and took me like half year to finally understand how AutoLayout works. Nowadays I can build a complex layout (like urs) without any problem. But **I've spent hours and hours reading and trying to figure it out**.
- AutoLayout isn’t magic but it’s magical. It does require you to think in abstract.
- I find doing it in code helped me understand what was actually going on rather than just relying on Xcode's suggested "fixes"
- AutoLayout is tough for complex layouts. Using Xcode to visually create constraints is awful. **So hard to update**. **"Xcode interface builder makes it difficult to update constraint if there is any changes"**
