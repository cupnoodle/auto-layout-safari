---
layout: post
title: Making Sense of Auto Layout
date: 2018-05-15 03:47 +0800
permalink: book-pitch
---

<style>
button,
input,
optgroup,
select,
textarea {
    margin: 0; /* 3 */
    color: inherit; /* 1 */
    font: inherit; /* 2 */
}
button {
    overflow: visible;
    border: none;
}
button,
select {
    text-transform: none;
}
button,
html input[type="button"],
/* 1 */
input[type="reset"],
input[type="submit"] {
    cursor: pointer; /* 3 */

    -webkit-appearance: button; /* 2 */
}
button[disabled],
html input[disabled] {
    cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
    padding: 0;
    border: 0;
}
input {
    line-height: normal;
}
input:focus {
    outline: none;
}

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
  background-color: rgba(253, 253, 253, 0.75);
  max-width: 800px;
}

.red{
  color: #D8141F;
}

.post-subscribe{
  margin-top: 2rem;
  margin-bottom: 2rem;
  margin-left: auto;
  margin-right: auto;
  max-width: 700px;

  padding: 1rem;
  border: 1px solid #CCC;
  text-align: left;
  border-radius: 4px;

  background-color: #FFF;
  border-top: 2px solid #338332;
  border-bottom: 2px solid #338332;

  box-shadow: 0px 0px 5px rgba(0,0,0,.3);
}

.post-subscribe h4{
  font-size: 1.2rem;
  font-weight: 700;
  margin-top: 0;
}


.post-subscribe input{
  font-size: 1rem;
  padding: 0.5rem; 
  border-radius: 3px;
  border: 1px solid #999;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;

  width: 100%;
}

.post-subscribe input[type="submit"]{
  font-size: 1rem;
  padding:0.5rem ; 
  background-color: #4caa33; 
  color: #f9f9f9;
  cursor:pointer;
  -webkit-border-radius: 5px;
  border-radius: 5px; 
  width: 100%;

  border: 0;
}

.post-subscribe input[type="submit"]:hover{
/*  background-color: #4BC948;
  color: #F9F9F9; */
}
</style>

A fundamental guide on learning Auto Layout

# "Whatever I try, it's either conflicting or when I finally got it all blue and think "**That's it!**", but then go to see it on another device, it all looks absolutely horrible."

You have spent weeks wrangling with Auto Layout trying to make your app looks good but Xcode keeps screaming at you with <span class="red">bright red lines</span> whatever you tried. 

You fear that 3 months of coding work is getting thrown away as you can't even get the user interface to work.

You picked up Swift and enjoyed learning it as it is easy to understand, but Auto Layout seems unreasonable to you. At this point it seems like it would be much easier if you just designed UI for every single iPhone and iPad by it self.

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

When you ask for advice on internet forum, you get different conflicting advices. "Ditch the Interface Builder, do Auto Layout in code!", "Use library like SnapKit!", "Try UIStackViews!". Which advice should you take? Should you spend extra time on learning third party library just to make the user interface work?

# What if you could bend constraints to your will and create user interface that render perfectly on any screen size?
What if you knew **exactly** which constraint to place for each element? You'd know how to troubleshoot whatever red lines Xcode has thrown at you. You'd be confident that your app will look exactly like you want it in all iPhones and iPads. **You could finish the app that you have been working on for 3 months and proudly ship it to the App Store**.

# Don't let Auto Layout stop you from shipping your first app to the App Store
Learn the fundamentals of how Auto Layout work and why Apple designed it this way. Understand Auto Layout and let it help you design user interface more efficiently and **ship your app** faster. You'd be able to brag about the app you just submitted to your friend, cousin and the barista, and have a better resume for applying iOS developer positions.

# Learn the fundamentals of Auto Layout
The problem with Auto Layout is that winging it as you go along is not an option. With coding you often can trial and error until it works, so we are used to it. Auto Layout needs to be properly understood and applied systematically, you have to understand what every single constraint is doing, throwing them in at random until its ‘<span style="color:#4691D6;">all blue</span>’ is never going to work.

_Making Sense of Auto Layout_ will explain the fundamentals of Auto Layout including how it decides an UI Element (UIView, UILabel etc) position and size, what problems do Auto Layout solve and why do Xcode shows you <span class="red">red lines</span> and how to troubleshoot them.

# What's in the book?
Instead of showing you a specific complex layout to follow step by step, this book will break down and explain the fundamentals of Auto Layout and let you connect the dots before you start designing your own layout. This book will focus on doing Auto Layout using Interface Builder (Xcode GUI), but its core concept can be applied to doing it programmatically (using code) as well.

- How User Interface is being designed prior to Auto Layout and why Auto Layout is introduced
- How Auto Layout determine position and size of a UI Element by using constraints you defined
- Why missing constraints (<span class="red">Red lines!</span>) appear and how to solve them
- Why conflicting constraints (<span class="red">Red lines, with numbers!</span>) happen and how to solve them
- What is intrinsic content size and the importance of it
- Using Tableview for content with dynamic length
- Using Scrollview for content with dynamic length
- What is constraint priority and when to use it
- What is content hugging and compression resistance
- Animating views with constraint

The book is currently work in progress, the final format with be a PDF with Xcode project exercise included.

# Testimonial on draft of the book
> "dude... wow... good job on this series! One of the best explanations I've read!"
>  -- [Alex Kluew](https://twitter.com/getaclue_1)

<div class="post-subscribe">
  <h4 data-drip-attribute="headline">Notify me when <i>Making Sense of Auto Layout</i> is launched</h4>
  <span style="font-size:1rem;"> 
    Get on the waiting list and receive discount code when the book is launched.<br /><br/>
  </span>
  <form action="https://www.getdrip.com/forms/295054774/submissions" method="post" data-drip-embedded-form="295054774">
    <div style="margin-bottom: 0.5rem;">
        <label for="drip-firstname">Name<span style="color:#952B45;">*</span></label><br />
        <input type="text" id="drip-firstname" name="fields[firstname]" value="" />
    </div>
    <div>
        <label for="drip-email">Email Address<span style="color:#952B45;">*</span></label><br />
        <input type="email" id="drip-email" name="fields[email]" value="" />
    </div>
    <div>
      <br>
      <input type="submit" value="Get on the waiting list" data-drip-attribute="sign-up-button" />
      <br><br>
      <span style="font-size: 0.8rem;">+ Bi-Weekly ish iOS Development tips.<br> Unsubscribe any time.</span>
    </div>
  </form>
</div>