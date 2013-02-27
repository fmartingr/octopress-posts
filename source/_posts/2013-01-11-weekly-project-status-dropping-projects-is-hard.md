---
comments: true
date: 2013-01-11 23:00:00
published: true
layout: post
slug: "weekly-project-status-dropping-projects-is-hard"
title: "Weekly project status: Dropping projects is hard"
categories: [Weekly project status]
---
{% img no-border center http://cdn.fmartingr.com/blog/uploads/global/weekly-project-status-banner.jpg %}
Since I wrote [the last post of 2012](/2012/12/31/2013/) I have been wondering if I could finish -or at least, work- on all the projects or experiments I wanted to. The answer was easy: **no**. I just don't have enough time for all the stuff I want to do, so I have made some decisions about my projects.
<!-- more -->
# Project *herobrine* ***…dropped!***

{% img center http://cdn.fmartingr.com/blog/uploads/2013/01/minecraft-database.png "Early draft of Project Herobrine" %}

The first time I did something about this project was like 2010, as some of you have guessed by the name of the project, its minecraft related.  It was intended to be a *wowhead-like* minecraft database but not only on PC.

Some features I wanted:  

- Developed with django, returning json objects to the client.
- Client MVC based with BackboneJS
- Responsive design -so you can check with your tablet while play on your computer-
- "no refresh" -backbone-
- WebGL/Canvas block rendering
- JS Redstone circuit maker
- JS Dye maker
- Homepage with random background featuring user's screenshots (above)
- Interactive crafting/brewing/...

Finally I have to say goodbye to this *jewel* -and it's really hard because I love minecraft and I wanted this to happen- because of various reasons: [minecraftwiki](http://minecraftwiki.net) already contains a lot of information -and it's really crowded-, the barrier of contents -I have to type in all the minecraft items, blocks, biomes, etc- and that this wasn't really a technical challenge -actually, some things are, but most of it are just database relations and stuff-.

I want to prepare a future post with all the work I made on this project. There's not much code but a lot of drafts and ideas that could help someone.

# Project *Serenity* ***…dropped!***
This was intended to be a way to simplify my jenkins business. Since I need a lot of tasks like: compile, minify, copy, deploy, upload, test… I wanted an app so I just define everything I need on a *YAML* file and call the app with `serenity <task>`.

I have some drafts built, a base YAML file, and some features planned like integrated tasks, custom tasks in the YAML file, configuration… 

Haven't coded for this one yet, but fortunately I heard about [grunt](http://gruntjs.com/) who may be something very close at what I wanted this one to be.

# ZombiePress ([github](http://github.com/fmartingr/zombiepress/)) ***…dropped!***
It's obvious. I was making my own blog software but since now I'm a proud octopress user this is no longer needed. I will keep the repo online just for making me feel nostalgic in the future.

# BlueBird ***…dropped!***
For all the iPad users… remember when Twitter changed the UI of the app? Did you remember the old one? I do. The new interface is **total crap**, the other was simply brilliant, and for me it was near the best one for an iOS app. I was hoping to get a clone working in javascript, but my knowledge of touch screens is not that good, I need to study more on the matter and then **maybe** I will try again, but I'm pretty sure some javascript guru will do something before that happens.

# Project *Amaranth*

The bigger brother. Recently I started a Vampire: Dark Age game with some friends and it remembered me to when I played rolegames over IRC. I started thinking that a online interface for roleplaying will be nice to have, because you can also use it in a live session to whisper, draw, etc. The brainstorm started quick enough for me to consider making it.

# Project *RTC*

Just born! -yesterday :P-. I want to make some kind of webRTC site to have conversations without the need of register, just create a conversation, get a link and you are set. It's more an experiment than a project itself.

# Uvepe8 ([github](http://github.com/fmartingr/uvepe8/))

I'm very proud -in a useful way- of this one and of course I'm maintaining it.

For the ones who don't know, its sort of *video-to-html5-canvas*, a mix between apple's and sublime text's, but mines support transparency -I needed it-.

There are some features I want to implement shown on the README file and a full code review.

# Dharma ([github](http://github.com/fmartingr/dharma/))

An application to check for 404 links on websites, a lot of things could be added to this, but for now is for playing around with threading, gevent and that kind of things.

---

I have some *other things* in mind I want to try, but that deserves another post -which is already in the works-.

Stay tuned for more updates, and as always, anything you want to say: comment, tweet, mail or shout at me!