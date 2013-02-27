---
comments: true
date: 2013-01-06 11:00:00
published: true
layout: post
slug: appsunday-sublimetext2
title: "#AppSunday: SublimeText 2"
categories:
- AppSunday
---

> Welcome to #AppSunday, my little weekly space on the blog to review and explore applications I use in my day to day.

As promised, welcome to the first *#AppSunday* of the year. This time I will look into **SublimeText 2**, a very good developing app you all will probably know already.
<!-- more -->
I've tried a lot of applications for developing. All we developers have. Looking for an application that fit your needs tend to be the worst part when it comes to software development.

I'm finally using SublimeText for every language except for python/django where I still use *pyCharm* from time to time -I think pycharm's code completion it's better than sublimetext's one-.

I'm giving the credit of knowing SublimeText to two individuals: first, [@juanriaza](http://twitter.com/juanriaza). Told me about this **a lot** of times, but I really never tested it until [@jgasteiz](http://twitter.com/jgasteiz) came to scene. Meet him on the 2012's google Hackaton where he was using SublimeText -the multiple cursor thingy- and I though… **I must try that**. 

# What is it?

Difficult question here. The easy answer is **a text editor**, but it's much more that that.  
It's not and IDE, but it is.  
It's complicated.

I say it as an **extendable advanced text editor**. Because it already have a lot of useful functions by its own -I will explain some later-, but also have [a lot of plugins](http://blog.fmartingr.com/2012/12/21/my-sublimetext2-workspace/) that are capable of extending the app functionality to a new level.

# What makes ST2 so special?

Before the screenshots and the features I need to say one thing about working with ST2: **focus on your keyboard, not your mouse**. The entire workflow with ST2 works this way, if you're afraid just don't be, you can be faster without using your mouse and this app it's really helpful with that. ST2 have key bindings for *almost* every command. With this in mind, the first feature:

> **Note**: From now on I will use OS X keybinds, if you're a Windows/Linux user, replace `CMD` with `Ctrl`.

## Command palette

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/command-palette.png "The command palette looking for the Install Package command" %}

**Keybind:** `CMD` + `SHIFT` + `P`  
Brings down a search menu with all the commands the application have. You can move with the cursor or use it's smart search to select the command you're looking for. As you can see in the screenshot you don't need to write down the whole command name, it just need some letters in the correct order.

## Go to anything

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/go-to-anything.png "Looking for a file that I don't remember where it is" %}

**Keybind:** `CMD` + `P`
You don't really need to look that path tree ever again. Just hide it and if you need to edit some file use the *go to anything* function, write the filename -or just some letters again, remember, smart search- and press enter. There you go, your file with just some key strokes.

You can also use a `:` or `@` statement to go directly to a line number or a method! Also, you can use `#` to search text within the file.

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/go-to-anything-2.png "Going to a specified method-line number" %}

## Multiple cursors

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/multiple-cursors.png "Fast refactoring" %}

**Keybind:** `CMD` + `D`  
One of the star features, the multiple cursors. Highlight a word and press the key bind to highlight the next occurrence, when you have all, write to edit all at the same time!

## Split editing

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/split-editing.png "Split editing" %}

ST2 comes with seven layouts: Single, two/three/four columns, two/three rows and four grid. You can change to anyone of this with a key combination, and another one to move the file from one view to another.

For example, in the picture, I used the *go to anything* to open the file, then pressed `CMD` + `ALT` + `2` to select the two columns view, and then `CTRL` + `SHIFT` + `2` to move the opened file to the second view. May sound complicated but it was like 2 seconds -or less- of key strokes.

I don't know if you can add more layouts or customize the default ones.

## Find with regular expressions

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-st2/find-regular-expressions.png "Search using regular expressions" %}

**Keybind:** `CMD` + `F` to find, then `ALT` + `CMD` + `R` to activate the regular expression search.

# Conclusion

I've shown you some of the features that make it a very great developing tool. There are much much more, but I can't afford being writing this post for days. Go to [the SublimeText 2 website](http://www.sublimetext.com/) to download and give it a try.

Take your first week as a transition one, since it will be different from what you're using right now, unless you're a *vi maniac*. Explore the features, customize your settings, develop in various languages and then decide. It is worth your skills?

Hope you enjoyed this post! As always, suggestions, bugs, *grammar fails*, etc to my twitter account or email. Thanks!
