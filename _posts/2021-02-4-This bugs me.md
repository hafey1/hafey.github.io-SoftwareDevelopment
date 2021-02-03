---
title: This bugs me
categories:
- General
feature_image: "https://picsum.photos/2560/600?image=872"
---

Today's blog comes in the form of some exercises from [Chapter 6 of Teaching Open Source](https://quaid.fedorapeople.org/TOS/Practical_Open_Source_Software_Exploration/html/ch-Debugging_the_Code.html). The chapter itself is about bugs in FOSS and how one would interact with bugs in the context of FOSS. The exercises come from sections 6.4, 6.5, 6.6, and 6.7.

#### 6.4 Exercise: Find the Oldest Bug In Your FOSS project
For my group's chosen project Zulip, the oldest bug is found on its issues page on github. It was opened on October 21, 2015 as issue #213 with the name: Firefox notification tracebacks on mobile Safari. Based on the comment history over the last 6 years, the bug seems to be a syntax issue that is caused by a certain type of web browser trying to recieve an object constructor from zulip's notifications. Doing a bit more research, more of an depreciation issue. The browser that encounters this error is chrome on an android platform. The fix outlined by the related post from the chromium community is to replace the functionality associated with the notification constructor with a service worker that will do the equivalent task in the case of interacting with chrome on android. It seems that issue was not solved because it is niche and the pull request that attempted to solve it did not contain reasonable testing.  

#### 6.5 Excercise: Create Your Bug Tracker Account
The cool part about Github is that it already has a system that can act as a bug tracker with its issues feature. I already have a github account!

#### 6.6 Reproduce a Bug
I used zulip's issues page to find a bug where a favorited message would still be available to a user even if the stream that the message was posted in was deleted. This made me think of a possible scenario for a similar bug coming from the searchbar so I tried to test if it was possible to find a message that was a part of a deactivated stream from a keyword search. And it turns out that it is possible. I believe this is a bug given the warnings that come with deleting a stream. So I have made a post and am currently waiting for some interaction to establish how to approach fixing it.  

#### 6.7 Bug Triage