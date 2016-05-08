---
layout: post
title:  "User testing VR Regatta"
date:   2016-05-08 17:00:00 +1100
categories: virtualreality sailing
---

*[Try VR Regatta and give us feedback!](http://sideloadvr.com/detail.php?id=10012)*

VR Regatta is a sailing game we are building for GearVR.

![VR Regatta](/assets/vr_regatta_with_logo.jpg)

This blog post will tell a short story of our journey so far, sharing what tests we have done and how the game evolved based on feedback.

First of all a big **THANK YOU to everyone in the community who helped us so far, giving up their time and offering feedback on how to make the game better**. We really value and need that help.

This article is mostly relevant to indie devs moonlighting on their VR projects, but hopefully everyone will find something interesting here.

## TLDR: VR User Testing tips

* Upload to SideloadVR and ask for help on [reddit](https://www.reddit.com/r/sideloadvr).

* Enable Unity Analytics.

* Show your work on meetups.

* Video record gameplay during tests.

* Playtest yourself.

* Consider a 3rd party service, like [FISHBOWL VR](https://www.fishbowlvr.com).

<!--more-->

## How it started

Before VR Regatta we've built two other sailing prototypes: ["Sail to Freedom"](http://sideloadvr.com/detail.php?id=214) and ["Point of Sail"](http://sideloadvr.com/detail.php?id=31).

After showing people "Point of Sail", they asked for an ability to sail around. Initially we were hesitant to the idea, being afraid of inducing simulator sickness. We've built a sailing prototype anyway and after some testing we discovered that it was fine, as long as we could maintain 60 frames per second. Initially we've built it with 3rd person sailing mode only, assuming this will be more comfortable. After [feedback on reddit](https://www.reddit.com/r/GoogleCardboard/comments/478vh6/looking_for_feedback_on_beta_version_of_sailing/d0bey9f) we added first person view, and to our surprise, it worked very well.

Using Unity Analytics we could see, among others things, that our retention was terrible. Pretty much no one was coming back to play the game again. We could also see that some people have spend some time in the game, sailing around (let's hope they had a better experience then [TwistedVR - warning: explicit language](https://www.youtube.com/watch?v=02OrMQAxwfg)).

Over Easter we've run an internal ["Sailing VR Jam"](http://blog.marineverse.com/vr/sailing/2016/03/28/sailing-vr-jam-video.html). Brainstorming what to do, we decided to try to tackle our retention problem. Our hypothesis: Racing with high scores will be something that will make people come back.

## Version #1

This is the first version we've built:

<iframe width="100%" height="315" src="https://www.youtube.com/embed/kKYEEjn8zB8" frameborder="0" allowfullscreen></iframe>

Using Analytics, we were tracking how many people start and finish their race. Problem: Over 50% of people didn't finish. But why? This is something that is very hard to figure out by just looking at the numbers.

Our hypothesis was, that maybe we needed some instructions, like "go around the buoy" so we added those. Looking at the metrics: not much improvement. Well, we needed to show the game to some people and see what's really going on.

## Meetup testing

Where to find people willing to test a VR game in development? Virtual reality meetup is a pretty good bet :-)

From previous user testing we knew, that when testing GearVR apps it's quite challenging to actually see what the user is going through (We usually don't carry around a laptop to take advantage of tools like [OVR Monitor](https://developer.oculus.com/documentation/mobilesdk/latest/concepts/mobile-remote-monitor/) ).

In preparation for the meetup we've build a simple tool that would let us see the position of a sailing boat on an iPad - "VR Party Mode":
<iframe width="100%" height="315" src="https://www.youtube.com/embed/_UeGYLAel1k" frameborder="0" allowfullscreen></iframe>

During the meetup the tool worked great and we could see (and hear) that people were struggling, not knowing how to operate the boat or why they couldn't go forward (sailing against the wind).

Our idea how to fix it: We need a sailing tutorial..

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Thank you for trying VR Regatta tonight. Our next goal - sailing tutorial :-) <a href="https://twitter.com/hashtag/indiedev?src=hash">#indiedev</a> <a href="https://twitter.com/hashtag/VirtualReality?src=hash">#VirtualReality</a> <a href="https://twitter.com/hashtag/Melbourne?src=hash">#Melbourne</a> <a href="https://twitter.com/hashtag/meetup?src=hash">#meetup</a></p>&mdash; MarineVerse (@MarineVerseVR) <a href="https://twitter.com/MarineVerseVR/status/720555438169841664">April 14, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## A sailing tutorial

This was our first attempt at a tutorial:

<iframe width="100%" height="315" src="https://www.youtube.com/embed/W-lYOnxkp3A" frameborder="0" allowfullscreen></iframe>

We asked for help in testing the tutorial on VR developers slack channel. Someone kindly offered it.

The person testing it didn't use headphones. We assumed the usage of headphones as you can see in the video. Our tester thought that something is broken, luckily for us we were still chatting on slack so we could instruct them to try with audio. Their feedback: "It's boring."

Based on the feedback, we've created a new version of the tutorial. This time much shorter (*time to action in seconds rather than minutes*) and with text instructions.

## More user testing

During a recent after work event we showed VR Regatta again. We had someone spend over ten minutes in the game. They weren't impressed and we were not exactly sure why (and we didn't use our Party mode view this time). Maybe racing around the buoy is not that exciting after all?

Luckily for us, we've recently integrated Oculus SDK and for this testing session we've enabled [video capture](http://www.roadtovr.com/natively-record-video-take-screenshots-gear-vr/).

So what happened? I guess we could have predicted that - our tester skipped the tutorial and went directly on to play the race. In the race he got quite lost, sailed way too far into the empty sea (*maybe we need **a wrong way** indicator?*).


## Making it more fun

Based on the previous playtest (and others, where we discovered that sailing against the wind is difficult for newbies) we decided to create an "Easy Race":

<iframe width="100%" height="315" src="https://www.youtube.com/embed/Nota1PZyRmo" frameborder="0" allowfullscreen></iframe>

In "Easy race" you have wind in your sails (blowing from behind you) and the track is clearly marked by golden stars. Collecting the stars gives you instant gratification.

Is it more fun? Is it easier? Finding people willing to playtest the game is hard. We've invented a platform to solve that problem. Then, after quick googling we've found an existing solution: Fishbowl VR. Exactly what we wanted, and they even offered the first test session for free.

Of course we took that offer :-) Looks like the tester smoothly sailed through the "Easy race". There were also things to improve that he pointed out, that we will be fixing soon.

## Try VR Regatta

<a href="http://sideloadvr.com/detail.php?id=10012">![VR Regatta](/assets/vr_regatta_landscape.jpg)<br/><br/>Please try VR Regatta and give us more feedback!

It's still work in progress and we are working on making it better. Your help makes it possible.

Contact us feedback(at)marineverse.com