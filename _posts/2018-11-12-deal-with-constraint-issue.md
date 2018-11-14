---
layout: post
title: "Are there any good tools to help deal with issues that result from bad or invalid Autolayout constraints?"
date: 2018-11-12 15:36 +0800
categories: safari
permalink: deal-with-constraint-issues
---

Source:  [https://www.reddit.com/r/iOSProgramming/comments/2km44a/are_there_any_good_tools_to_help_deal_with_issues/](https://www.reddit.com/r/iOSProgramming/comments/2km44a/are_there_any_good_tools_to_help_deal_with_issues/)



## Pain

Are there any good tools to help deal with issues that result from bad or invalid Autolayout constraints?



Autolayout is the bane of my existence.



You can get practically everything right and then not be aware of some minor quirk and be stuck on the layout for a while.



things just go wrong (in Auto Layout).



**OP in comments:**

How do you deal with multiple screen sizes? 4S vs. 5 vs. 6 vs. 6 Plus

How does this work with size classes? 



### Why does this post exist?

OP is fed up with dealing with Auto Layout constraints.

OP doesn't understand Auto Layout.



## Jargon

Auto Layout

Constraints

Masonry

Pure Layout



## Recommendation

**Best advice is to ditch Auto Layout completely**. The amount of time wasted on it is absurdly disproportionate to the scale of the problem it's trying to solve.



**Learn to properly use auto layout. Trust me, it's worth it,** though yeah, can take a while (specially if you have to write it instead of using IB). I don't dare make UIs without it now.



 I agree the error messages (if you get one) on NSLayoutConstraints are practically useless.



## Worldview

"Many iOS Dev don't agree with me on ditching Auto Layout and do it manually"

"Auto Layout is over-engineered and using it create more issue than solution"



"Understanding Auto Layout takes time but it is worth it"

"Don't dare to write UI without using Auto Layout now"

" I find it good to not have to worry about independent screen sizes or orientations with Auto Layout."



"App should look good on multiple screen sizes and orientation"



"error messages (if you get one) on NSLayoutConstraints are practically useless"

