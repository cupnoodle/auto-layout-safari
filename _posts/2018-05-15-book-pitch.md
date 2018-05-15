---
layout: post
title: Making Sense of Auto Layout
date: 2018-05-15 03:47 +0800
permalink: book-pitch
---

<style>
.drop-shadow{
  -webkit-box-shadow: 0px 4px 12px -1px rgba(156,156,156,1);
  -moz-box-shadow: 0px 4px 12px -1px rgba(156,156,156,1);
  box-shadow: 0px 4px 12px -1px rgba(156,156,156,1);

  border-radius: 6px;
}

.how{
  display: block;
  font-size: 3em; 
  position: relative; 
  top: -6em;
  transform: rotate(-20deg); 
  -ms-transform: rotate(-20deg); 
  -webkit-transform: rotate(-20deg);
}
</style>

A fundamental guide on learning Auto Layout

# "Whatever I try, it's either conflicting or when I finally got it all blue and think "**That's it!**", but then go to see it on another device, it all looks absolutely horrible."

You have spent weeks wrangling with Auto Layout trying to make your app looks good but Xcode keeps screaming at you with <span style="color: #D8141F;">bright red lines</span> whatever you tried. 

You fear that 3 months of coding work is basically getting thrown away as you can't even get the user interface to work.

<div style="text-align: center;">
  <img class="drop-shadow" src="https://iosimage.s3.amazonaws.com/autolayoutbook/red_lines.png" alt="red lines" />
</div>

<br><br>

# "I think I’ve watched and read about 30 tutorials on AutoLayout up to now"

You have watched a bunch of Youtube video tutorials and when you go to try it on Xcode, you have no idea what you're doing.
Sometime you managed to do the layout shown in the video, but when it comes to your own layout, you're clueless. "I mean, on some UIViewControllers with a button and a label like in those tutorials, no problem at all. **But for setups like these?**"

<div style="text-align: center;">
  <img class="drop-shadow" src="https://iosimage.s3.amazonaws.com/autolayoutbook/complex_layout.png" alt="complex layout" />
  <div class="how">How do I even?</div>
</div>

When you ask for advice on internet forum, you get different conflicting advices. "Ditch the Interface Builder, do Auto Layout in code!", "Use library like SnapKit!", "Try UIStackViews!". Which advice should you take?

# What if you could bend constraints to your will and create user interface that render perfectly on any screen size?
What if you knew **exactly** which constraint to place for each element? You'd be confident to troubleshoot whatever red lines Xcode has thrown at you. **You could finish the app that you have been working on for 3 months and proudly ship it to the App Store**.

# Don't let Auto Layout stop you from shipping your first app to the App Store
Learn the fundamentals of how Auto Layout work and why Apple designed it this way. Understand Auto Layout and let it help you design user interface more efficiently and ship your app faster.