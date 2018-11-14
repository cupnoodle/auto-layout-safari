---
layout: post
title: "Interface Builder + Auto layout is such a tedious system for designing views"
date: 2018-11-12 15:36 +0800
categories: safari
permalink: interface-builder-tedious
---

Source : [https://www.reddit.com/r/iOSProgramming/comments/9qcuei/interface_builder_auto_layout_is_such_a_tedious/](https://www.reddit.com/r/iOSProgramming/comments/9qcuei/interface_builder_auto_layout_is_such_a_tedious/)



## Pain

Seriously it (Auto Layout) is harder than writing the code for the app!

To begin with interface builder doesn't provides even the most rudimentary design/layout tools that you would expect from such a system.



It also behaves in the most unexpected ways: select an item in the Document Inspector you would expect that you can then move it around with the arrow keys, but nope, it starts selecting other items in the list instead. 



You want to move and item on top of another but don't want to place it inside of it, well, have to do it manually with the arrow keys or changing the x/y value can't just drag it. 



Selecting specific items from the view (say you want to select the stackview itself and not one of it's items) is also very troublesome It is such a weird system.



**Auto layout is just insane**. I spent nearly an hour trying to figure out why a vertical stackview that I had with labels simply refused to expand it's width when I pinned it 16 p from the left and the right.



For some **insane** reason a subview of another view (which I couldn't see happening at first due to it having no background color) that the stackview was not a part of was shrinking to the current width of the stackview when I added constrains to the stackview and was thus preventing the stackveiw from expanding to the desired width.



You apply constraints to one item and the thing then adds a bunch of constrains to other items making it hard to keep track what exactly you are doing and then it shows you a bunch of errors/warnings with suggestions like "Add missing constrains" which if you use will only make your layout worst.



**What a cumbersome system**. Stuff like HTML/CSS, Android with it's XML or even React Native with it's XML/CSS like system are so much easier and intuitive for layout views. Trying to do anything beyond having more than a couple of items in Interface Builder + Auto layout is an exercise in frustration.



### OP in comments

I mean, in theory Auto layout is not a hard model to grasp but in practice it behaves in the most unexpected ways.



Have done a couple of apps already but the IB+AL part to try and make the app adapt to the different sizes is really tedious.



### Commenter pain

When talking about one view: you can make a 'complex' UI layout for all screen sizes and all orientations, using a single storyboard (given that iPad and iPhone designs are not drastically different) much much faster than **it would take someone to code that same layout**.



You talk about CSS, but even there you need to write a lot of separate rules to make sure the website looks good across multiple screen sizes



The disadvantages of doing everything in code are obvious, of course. You loose the advantages of seeing everything in Interface Builder, and it's slower to type everything. Plus, your view controllers tend to fatten up with repetitive code.



I remember learning auto layout and thinking it was tedious as well



The editor do behave quite *interesting* in many cases where  you expect it to behave nicely



I'll admit that it's not the funnest thing in the world to learn, but the reality is that with all the different sizes out there, it's not going to be easy to address all the issues.



Quality UI implementation in iOS has a rather steep learning curve. The lifecycle of viewcontrollers is another example.



Coming from Android its an absolute nightmare, you are used to putting something in a spot and not having the interface move it to the opposite side for no reason. 

I have gotten more used to it over time, I can still build an Android interface in half the time as iOS but I also dont spend the hours that I used to dealing with it. For me, what helped me the most was: 

A: Not using stack views, they behave too strangely

B: Not using auto layout, I would rather spend the time setting things myself than fixing the auto layout nonsense.



## Jargon

Interface Builder

Auto Layout

view

Document Inspector

StackView

Labels

Constraints

Error

Warning

"Add missing constraint"

HTML

CSS

Android

XML 

React Native

superview

Safe Area

programmatically

flexbox

NativeScript

Button

viewDidLoad

Version Control

VFL / Visual Format Language

NSLayoutConstraint

Anchors

Container view

Layout priorities

Multipliers

Compression Resistance

Content Hugging Priorities

Content Compression Resistance

IBInspectable

IBDesignable



## Recommendation

It (Auto Layout) behaves depending on how you set the constraints and how those constraints translate their relationships to other views/constraints that you have not set. When you don't set everything up properly, then it will behave unexpectedly. Taking the time to think through how things should be laid out and what should happen on all screen sizes at the beginning and creating the constraints that way will make life easier.



An easy way to do things is to chunk them in groups - so if I have a UI section that has, say, a button, a switch and some text, you drop those into a view and set their constraints to behave in that view. Then you set the view's constraints in relation to its parent views. This way, you can work top-down or bottom-up for your constraints, but it ensures that everything has a minimally 4 way (read, constraint) relationship with the other views around and, eventually, the superview or Safe Area.



------

How about **programmatically layout** out your views? On some projects I've done, the client required we not use Interface Builder, but instead add all views and constraints by code. It's a bit more precise, and once you get the hang of it, you'll fall into a rhythm.



The disadvantages of doing everything in code are obvious, of course. You loose the advantages of seeing everything in Interface Builder, and it's slower to type everything. Plus, your view controllers tend to fatten up with repetitive code.



------

Here are some tips: - In general, each object needs a minimum of 4 constraints - You can set a left, right, and top constraint on a label and the number of lines to 0, and its height will auto adjust to the content. - Build the layout and constraints one object at a time. I like to create a mock up of the design first and work from that. - “Group” parts of a view by adding them in a “container “ UI View. The constraints on the objects inside will remain if you need to change the layout of the entire view later.



------





## Worldview

We used to use the phrase, “Works as designed.” That is, it works the way the person who designed it expected, even if it’s not the way you expect it to work.

It is the way it is. Wanting things to be different than they are is a recipe for frustration.



------



I guarantee you, once you get some experience with it doing more complex stuff, you'll see it's value. When talking about one view: you can make a 'complex' UI layout for all screen sizes and all orientations, using a single storyboard (given that iPad and iPhone designs are not drastically different) much much faster than it would take someone to code that same layout. 



"Using Auto Layout to design layout is much faster than coding them manually"



------



Have you ever tried creating a screen that looks good across multiple devices programatically? That's hard, no matter what you build it with.



"Creating an UI that looks good across multiple devices is hard"

"iOS's constraints are really as intuitive as it gets"



------


CSS and flexbox can really drive me up a tree sometimes. In those situations I’ve caught myself thinking, “if only I had autolayout I’d be done already!”



"iOS's Auto Layout is easier than CSS / flexbox"

------



The editor(Interface Builder) do behave quite *interesting* in many cases where you expect it to behave nicely.
"Interface builder may give unexpected output sometimes"

------



The reality is that **we have several different screen sizes and everyone has portrait and landscape**. You also now have **multi-tasking** on some that will change the screen size.



If you try to do everything without auto layout and the size class, you'll probably have even more frustration.



EVERYTHING you do in IB can be done in code. "Every UI can be done using code"



It's not the funnest thing in the world to learn, but the reality is that with all the different sizes out there, it's not going to be easy to address all the issues.



"Learning Auto Layout is not exactly fun, but it is the best solution to address all the different screen sizes"

------



"Doing AutoLayout in Interface builder is so much easier than in code".



"Doing AutoLayout in code is so much easier than in interface builder".

------



Quality UI implementation in iOS has a rather steep learning curve.

------



