---
layout: post
title: "I'm giving up on Auto Layout"
date: 2018-05-11 15:36 +0800
categories: safari
permalink: cant-wrap-head-around-autolayout
---

Source: [https://www.reddit.com/r/iOSProgramming/comments/3lmc20/im_giving_up_on_auto_layout/](https://www.reddit.com/r/iOSProgramming/comments/3lmc20/im_giving_up_on_auto_layout/)

## Pain

- I've been battling with auto layout since I picked up iOS dev a couple of months ago
- at this point **I think it's just not worth it anymore** 
- when I tried to add a view to it with CGRectMake, **it doesn't work**
- To me **auto layout constraints make very little sense** when it comes to compatibility with setFrame and animation.
- if that doesn't work, well **I guess I'll probably just give up on iOS dev**
- I was just really frustrated with auto layout because it seems really straight forward in IB, but **whenever I try to add animation or a subview (programmatically), it always gets screwed up.**

Commenter's 
- Well, and everything screams bright red when something's wrong. (In Interface Builder)
- I hate autolayout, when i started programming i wasted 1 month on that shit, its horrible for beginners 
- I can not understand when someone says its nicer to do views in autolayout then in code. autolayout is such a strange and screwed abstraction, just the idea that you do part in code and part in IB is grrrrrrr.
- (Auto Layout) Its more frustrating than code signing and developer certificate errors.
- In autolayout you plaster the views in the IB like a 5 year old child and then you have to select and enter 100 constrains and create a useless buggy mess.

## Jargon

- Auto Layout
- project
- scene
- constraint / auto layout constraint
- view
- CGRectMake
- vertical constraint
- subview
- setFrame
- animation


## Recommendations / Buys

- Avoid using setFrame, setCenter, setBounds, etc. if you're using Auto Layout
- I recommend doing Auto Layout in Interface Builder, at least while you're learning. It's generally easier to learn there because you can see the relations. You'll also be able to see how constraints affect each other and receive warnings / errors for what's wrong.
- I did a video answering some common Auto Layout scenarios for people who asked in this sub a few months ago. [Here's a link](https://www.youtube.com/watch?v=Gl6DibzPYa4) in case you're interested.
- Once you grasp the intention and thought process behind Auto Layout it's incredibly nice. There are a ton of people here who are happy to answer questions as you encounter problems.
- (There are some open source wrappers for Auto Layout....I find them to make the situation worse, especially as you're learning. I would avoid trying to find a workaround until you're proficient in Auto Layout.)
- **"Don't use wrapper / library for Auto Layout"**
- Just like views, you can make IBOutlets of constraints that you created in Interface Builder.
- In animation blocks, manipulate the -constant property of these constraints. Don't add new ones or remove them unless it's the only option.
- After changing the constraint, call -layoutIfNeeded on the superview of any view you modified inside your animation block. This will animate your changes.
- Don't use setFrame, setCenter, setBounds.
- I typically try to do all my views in IB or all my views in code when possible, even if it means having one hidden most of the time. There's always the occasion to mix and match...but its easier when you can avoid it.
- Try to use Auto Layout (no manual frames) as much as possible, even in programmatic creations (turn on Auto Layout). Sticking with 1 layout methodology (rather than mixing) is generally more straight-forward.

- **Either manipulate frame or constraints**. **Don't fight the system** and set a frame when you have constraints, they will win.
- just add some constraints to it and animate it with constraint changes. Remember to call layoutIfNeeded within the animation block if your animating constraint changes.
- With iOS9+ it is recommended that you use stackViews as much as you can.
- You still need to learn auto layout but stackViews make some complex layouts easier to build
- You can't give up on auto layout, it will make development harder.
- Watch some WWDC session videos on auto layout from the previous years, you will have a better understanding
- 🔥🔥🔥 I also recommend not taking advice from people telling you that auto layout sucks or to not use it, these are probably people who did not take the time to understand the system and thus just tell others it is not worth it.

- look into SnapKit if you plan on doing your autolayout in code.
- Check the documentation of UIView or it's OS X counter part NSView. 

- Autolayout + IB is the shit once you actually take the time to experiment and learn the fundamentals
- My guess is you just hacked around and rushed through it without trying to learn properly. These are highly powerful tools that every iOS dev should understand and use in my opinion.

## Worldview








