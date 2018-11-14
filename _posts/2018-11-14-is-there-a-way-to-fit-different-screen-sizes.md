---
layout: post
title: "Is there a good tutorial/video/other source specifically for making your app display at variable sizes to fit different screen sizes??"
date: 2018-11-14 15:36 +0800
categories: safari
permalink: is-there-a-tutorial-for-fitting-different-screen-sizes
---

Source: [https://www.reddit.com/r/iOSProgramming/comments/987a1e/is_there_a_good_tutorialvideoother_source/](https://www.reddit.com/r/iOSProgramming/comments/987a1e/is_there_a_good_tutorialvideoother_source/)



## Pain

Is there a good tutorial/video/other source specifically for making your app display at variable sizes to fit different screen sizes?



I've done a few tutorials and built a simple app of my own, but it was built to fit my iPhone SE and doesn't suit any other screen size.



I assume **I could have started off in a completely different way** and built it to be variable (font sizes, object widths etc) from the start?



How can I go back to this design now and convert it so that it naturally adapts to the screen of iPads, bigger phones etc?



## Why OP is posting this?

OP's app doesn't suit screen sizes other than his own iPhone SE

OP want to make his app looks good across all screen sizes.



## Jargon

app

variable size

iPhone

iPad



## Recommendation

[https://www.raywenderlich.com/492-adaptive-layout-tutorial-in-ios-11-getting-started](https://www.raywenderlich.com/492-adaptive-layout-tutorial-in-ios-11-getting-started) is a good tutorial (size classes)



------

Check out **Ray Wenderlich’**s content on auto layout. That will help you achieve what your are looking for.



------

You need to learn how to do constraints.



------

The broad topic you're looking for is called adaptive layout. There are three concepts within this you should research:

1. Auto layout and constraints
2. Size classes
3. Stack views



- The [Ray Wenderlich tutorial](https://www.raywenderlich.com/492-adaptive-layout-tutorial-in-ios-11-getting-started) others have mentioned is a good one, it goes into auto layout and size classes.
- [WWDC video on auto layout techniques](https://developer.apple.com/videos/play/wwdc2017/412/) - this goes into auto layout and stack views.
- I wrote a tutorial on size classes [here](https://medium.com/@craiggrummitt/size-classes-in-interface-builder-in-xcode-8-74f20a541195).





## Worldview

App should look good in all screen sizes



Prefer learning through tutorial / video



Build for own phone size first